# Cursor Usage

Cursor can be used to open, develop, run and debug this repository.

## Open locally

``` bash
git clone <PRIVATE_REPOSITORY_URL>
cd <REPOSITORY_DIRECTORY>
```

Open that directory in Cursor and select the Python interpreter from the
project's `.venv`.

## Configure the project

Create `.env` locally from `.env.example` and supply your own GitHub
token. Never paste a real PAT into source code, README content or an AI
prompt.

## Run/debug

Use the same project entry point documented for local execution:

``` bash
python main.py
```

Use `python main.py --help` if the checked-in implementation exposes CLI
arguments.

## MCP from Cursor

If the installed Cursor version supports MCP, configure it to
start/connect to the same MCP server entry point:

``` text
mcp_integration/server.py
```

The exact client-side MCP settings can change between Cursor versions,
so use the MCP configuration UI/schema provided by the installed Cursor
build rather than copying an unverified client-specific path from this
document.

The conceptual connection remains:

``` text
Cursor -> MCP server -> Python repository-analysis workflow -> repository intelligence
```
