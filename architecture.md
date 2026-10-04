# Architecture

## Purpose

The project separates repository fact extraction from conversational
presentation. Python modules inspect the repository and derive technical
information. MCP exposes the repository-analysis capability to supported
AI clients. Claude can then request the analysis and present the results
in natural language.

## Architecture diagram

``` mermaid
flowchart TD
    A["Engineer"] -->|Repository URL + question| B["Claude / MCP-capable client"]
    B -->|MCP tool call| C["mcp_integration/server.py"]
    C --> D["main.py"]
    D --> E["ingestion.py"]
    E --> F["scanner.py"]
    F --> G["static_analysis.py"]
    G --> H["architecture_analysis.py"]
    H --> I["runtime_flow_analysis.py"]
    I --> J["code_flow_analysis.py"]
    J --> K["compatibility.py"]
    K --> L["report_writer.py"]
    K <--> M["compatibility_enricher.py"]
    M --> N["version_utils.py"]
    M <--> O["External version/package information"]
    L --> C
    C --> B
    B --> P["Natural-language answer"]
```

## Responsibilities

### Workflow layer

`main.py` controls the complete analysis and calls the required modules
in sequence.

### Repository intake

`ingestion.py` takes the GitHub repository and prepares it for the
analysis workflow.

### Discovery

`scanner.py` creates an inventory of source, dependencies,
configuration, tests, infrastructure and other relevant artifacts.

### Static facts

`static_analysis.py` derives technologies, dependencies, APIs, tests,
external calls and repository-type information from repository evidence.

### Architecture

`architecture_analysis.py` analyzes packages, modules, imports,
functions, classes, entry points and relationships to derive the
component view.

### Runtime and code flow

`runtime_flow_analysis.py` analyzes application startup/execution
behavior where present. `code_flow_analysis.py` connects entry points,
handlers, services/use cases, repositories, clients/DAL and
database/external calls where those constructs exist.

### Dependency intelligence

`compatibility.py` bridges dependency/version facts found in the
repository with external version enrichment. `compatibility_enricher.py`
retrieves current information where available, and `version_utils.py`
normalizes/computes statuses such as `CURRENT`, `UPDATE_AVAILABLE`,
`AHEAD_OF_LATEST` and `UNKNOWN`.

### LLM explanation

`llm_analysis.py` is selective and works on already collected analysis
information for higher-level summaries/use cases/explanations. It is not
the primary source of low-level repository facts.

### Reporting

`report_writer.py` combines the outputs of the analysis stages into
repository intelligence that can be stored/retrieved through MCP.

### MCP

`mcp_integration/server.py` exposes repository-analysis capabilities as
MCP tools and is the bridge to Claude Desktop.
`mcp_integration/client.py` isolates MCP communication from core
analysis logic.

## Repository-type behavior

The scanner first identifies the files and technologies that actually
exist. Static analysis uses that evidence to understand the repository
content/type. Application repositories can proceed through
architecture/runtime/code-flow analysis; Terraform/EKS-style
repositories should receive infrastructure-focused analysis rather than
a fabricated application flow.

## Trust boundary

Repository facts should come from repository analysis. Changing external
version information should come from the enrichment path when reliable.
If information cannot be verified, the system should represent it as
unknown rather than inventing a result.

## Future integration direction

This architecture is intentionally modular so the repository
intelligence can later be incorporated into a broader GitHub/Orion-style
product experience without coupling the analysis engine to one user
interface.
