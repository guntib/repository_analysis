# Local Setup and Run Guide

## Prerequisites

-   Git
-   Python version compatible with the checked-in project
-   access to the private repository
-   a GitHub credential/PAT with only the permissions required for
    repositories you are authorized to analyze
-   Claude Desktop only if testing the Claude/MCP path

## Clone

``` bash
git clone <PRIVATE_REPOSITORY_URL>
cd <REPOSITORY_DIRECTORY>
```

## Virtual environment

macOS/Linux:

``` bash
python3 -m venv .venv
source .venv/bin/activate
```

Windows PowerShell:

``` powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

## Install dependencies

If `requirements.txt` is present:

``` bash
pip install -r requirements.txt
```

Use the dependency mechanism checked into the repository if it differs.

## Environment

Copy the example:

``` bash
cp .env.example .env
```

Set:

``` dotenv
GITHUB_TOKEN=your_own_github_token
```

Do not commit `.env`.

## Run

The project documentation identifies `main.py` as the main workflow
controller:

``` bash
python main.py
```

If the current implementation requires parameters:

``` bash
python main.py --help
```

Use only arguments supported by the checked-in code.

## Validate

A clean validation should prove:

1.  repository access succeeds
2.  scanning discovers the expected files
3.  static analysis identifies technologies/dependencies
4.  architecture/flow analysis runs where applicable
5.  the report is produced
6.  the MCP server starts
7.  Claude can see and call the MCP tool
8.  the response reflects repository-derived information

## Security validation

Before sharing:

``` bash
git status
git log --all --oneline
```

Also inspect the repository/history for accidentally committed
credentials using your organization's approved secret-scanning process.
If a real PAT was ever committed, revoke/rotate it.
