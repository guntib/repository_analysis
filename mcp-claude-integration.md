# Claude Desktop and MCP Integration

## Integration model

``` text
Claude Desktop
      |
      | MCP tool request
      v
mcp_integration/server.py
      |
      | calls repository-analysis workflow
      v
main.py -> analysis modules -> report
      |
      | repository intelligence
      v
MCP Server
      |
      v
Claude Desktop
      |
      v
Natural-language answer
```

The important distinction is that Claude is the conversational layer.
Repository facts are derived by the Python analysis workflow and exposed
through MCP.

## Server entry point

The documented MCP server is:

``` text
mcp_integration/server.py
```

## Claude Desktop configuration

Configure Claude Desktop to invoke the MCP server. A typical local stdio
configuration has the following shape:

``` json
{
  "mcpServers": {
    "repository-analysis": {
      "command": "<ABSOLUTE_PATH_TO_PYTHON>",
      "args": [
        "<ABSOLUTE_PATH_TO_REPOSITORY>/mcp_integration/server.py"
      ]
    }
  }
}
```

Replace the placeholders with local absolute paths.

Important: configuration details can vary by Claude Desktop/MCP version
and by how `server.py` is implemented. The repository's actual server
implementation is authoritative.

## GitHub authentication

The repository-analysis layer may require GitHub access. Keep the
PAT/token outside source code:

``` dotenv
GITHUB_TOKEN=your_own_github_token
```

Use a local `.env` or an approved secret mechanism supported by the
implementation. Never commit the token.

## Test sequence

1.  Activate the project's Python environment.
2.  Confirm dependencies are installed.
3.  Confirm the required GitHub environment variable is available to the
    MCP process.
4.  Configure Claude Desktop with the MCP server.
5.  Restart Claude Desktop.
6.  Confirm the repository-analysis tool is visible.
7.  Ask Claude to analyze an authorized test repository.
8.  Confirm the tool is invoked and the response matches the repository
    analysis.

## Example prompt

``` text
Analyze this repository: <REPOSITORY_URL>

Give me:
- repository purpose and structure
- technologies/frameworks
- architecture and major components
- runtime/code flow
- dependencies and versions
- APIs and external integrations
- tests
- infrastructure
- any dependency update/compatibility information that can be reliably verified

Use the repository analysis as the source of technical facts. Clearly identify anything that cannot be determined.
```

## What happens behind the scenes

1.  Claude receives the engineer's request.
2.  Claude invokes the MCP repository-analysis tool.
3.  `server.py` routes the request to the Python analysis workflow.
4.  `main.py` coordinates repository intake, scanning, static analysis,
    architecture/flow analysis, dependency analysis and reporting.
5.  MCP returns the resulting repository intelligence.
6.  Claude turns that intelligence into a conversational answer.

## Troubleshooting

If Claude cannot see the tool:

-   verify the configured Python path
-   verify the absolute path to `server.py`
-   verify the Python environment contains project dependencies
-   restart Claude Desktop after configuration changes
-   check MCP/server logs for startup errors

If GitHub access fails:

-   confirm the token is present in the MCP process environment
-   confirm the token has access to the requested private repository
-   confirm the token has not expired/revoked
-   do not print the token while troubleshooting
