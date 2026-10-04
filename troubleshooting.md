# Troubleshooting and Handoff Checklist

## Local analysis does not start

-   activate the correct virtual environment
-   install the repository's dependencies
-   run the documented entry point
-   inspect the actual traceback rather than changing configuration
    blindly

## Private GitHub repository cannot be accessed

-   verify the GitHub credential exists in the process environment
-   verify repository authorization/permissions
-   verify the credential has not expired
-   never log or print the full credential

## MCP server does not appear in Claude

-   verify the MCP configuration syntax
-   use absolute paths for Python and `mcp_integration/server.py`
-   verify the selected Python environment contains required packages
-   restart Claude Desktop
-   inspect MCP startup logs

## Analysis differs by repository type

This is expected. Application repositories may expose runtime/code-flow
relationships. Infrastructure repositories may expose
Terraform/Kubernetes/cloud relationships instead. The analyzer should
not invent application flows that do not exist.

## Dependency version cannot be verified

Use `UNKNOWN` rather than guessing. Repository analysis establishes the
version used in the code; external enrichment establishes current/latest
information only when a reliable source is available.

## Before sharing the repository

-   [ ] README renders correctly
-   [ ] architecture diagram is visible
-   [ ] `docs/` is committed
-   [ ] setup works from a clean clone
-   [ ] `.env` is ignored
-   [ ] `.env.example` contains placeholders only
-   [ ] no PAT/API key is present in code, docs, screenshots or Git
    history
-   [ ] MCP server starts successfully
-   [ ] Claude can call the repository-analysis tool
-   [ ] one authorized sample repository works end-to-end
