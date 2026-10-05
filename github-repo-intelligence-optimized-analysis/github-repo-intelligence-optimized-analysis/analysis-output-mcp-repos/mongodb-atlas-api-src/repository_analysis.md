# Repository Intelligent Analysis Report

## 1. Repository Summary

- **Repository:** mongodb-atlas-api-src
- **Source:** https://github.com/NBCUDTC/mongodb-atlas-api-src.git
- **Source Type:** GitHub
- **Repository Type:** Application / Service / Library Repository
- **Files Analyzed:** 188
- **Local LLM Status:** Skipped by command line

### What the Application / Repository Does

This tool makes use of Atlas APIs to fetch logs and metrics for multiple NBCUDTC Peacock projects and push them onto Loki and Grafana respectively making it easier for anyone within the organization to get access to MongoDB operational data. There are 6 microservices in this repository all pulling information about MongoDB either from Github or Atlas. The 6 microservices are: 1. atlas-cost-gcs-exporter - This microservice pulls information about MongoDB Atlas cost and pushes it to GCS for FinOps. 1. The production FinOps bucket is mongo-atlas-cloud-cost. 2. We have previously worked with Ying Tao [ying.tao@sky.uk] to grant access to the bucket. 3. Potential improvement is to use workload identity to access the bucket instead of a GCP key provided by FinOps. 2. atlas-cost-usage-exporter - This microservice pulls information about MongoDB Atlas cost and exposes a JSON API for Grafana dashboards. 1. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/mongodb-atlas-cost-visibility 3. github-db-driver-version-exporter - This microservice pulls information about MongoDB drivers from Github and pushes it to Prometheus.

### Repository Summary

This tool makes use of Atlas APIs to fetch logs and metrics for multiple NBCUDTC Peacock projects and push them onto Loki and Grafana respectively making it easier for anyone within the organization to get access to MongoDB operational data. There are 6 microservices in this repository all pulling information about MongoDB either from Github or Atlas. The 6 microservices are: 1. atlas-cost-gcs-exporter - This microservice pulls information about MongoDB Atlas cost and pushes it to GCS for FinOps. 1. The production FinOps bucket is mongo-atlas-cloud-cost. 2. We have previously worked with Ying Tao [ying.tao@sky.uk] to grant access to the bucket. 3. Potential improvement is to use workload identity to access the bucket instead of a GCP key provided by FinOps. 2. atlas-cost-usage-exporter - This microservice pulls information about MongoDB Atlas cost and exposes a JSON API for Grafana dashboards. 1. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/mongodb-atlas-cost-visibility 3. github-db-driver-version-exporter - This microservice pulls information about MongoDB drivers from Github and pushes it to Prometheus.

## 2. Technology Stack

- **Languages:** Terraform, Go, Python
- **Frameworks:** Not detected
- **Runtime:** Go 1.25.11
- **Databases:** MongoDB
- **Cloud Platforms:** Google Cloud
- **Containers:** Docker, Docker Compose
- **Kubernetes Helm Terraform:** Helm, Terraform
- **Ci Cd:** GitHub Actions
- **Testing Tools:** Testify
- **Monitoring Observability:** Prometheus
- **Important Core Libraries:** github.com/beorn7/perks, github.com/cespare/xxhash/v2, github.com/davecgh/go-spew, github.com/go-co-op/gocron, github.com/golang/protobuf, github.com/golang/snappy, github.com/google/uuid, github.com/klauspost/compress, github.com/matttproud/golang-protobuf-extensions, github.com/mongodb-forks/digest, github.com/montanaflynn/stats, github.com/pmezard/go-difflib, github.com/prometheus/client-golang, github.com/prometheus/client-model, github.com/prometheus/common, github.com/prometheus/procfs, github.com/robfig/cron/v3, github.com/stretchr/objx, github.com/stretchr/testify, github.com/xdg-go/pbkdf2, github.com/xdg-go/scram, github.com/xdg-go/stringprep, github.com/youmark/pkcs8, go.mongodb.org/atlas-sdk/v20240805004, go.mongodb.org/mongo-driver, go.uber.org/atomic, golang.org/x/crypto, golang.org/x/sync, golang.org/x/sys, golang.org/x/text, google-cloud-storage, google.golang.org/protobuf, gopkg.in/yaml.v3, python-dateutil, python-dotenv, requests

## 3. Repository Scan and Engineering Artifacts

- **Important files:** .github/workflows/build-atlas-cost-gcs-exporter.yaml, .github/workflows/build-atlas-cost-usage-exporter.yaml, .github/workflows/build-github-db-driver-version-exporter.yaml, .github/workflows/build-mongodb-atlas-api.yaml, .github/workflows/build-mongodb-atlas-exporter.yaml, .github/workflows/build-mongodb-github-driver-version-exporter.yaml, .github/workflows/build-mongodb-version-tracking-exporter.yaml, .github/workflows/go-unit-test.yaml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/pr-reviews.yaml, .github/workflows/pr-title-validation.yaml, .github/workflows/set-self.yaml, .github/workflows/setup-repository.yaml, README.md

- **Configuration:** atlas-cost-usage-exporter/config.yaml, mongodb-atlas-api/config.yaml
- **Docker:** atlas-cost-gcs-exporter/Dockerfile, atlas-cost-gcs-exporter/docker-compose.yaml, atlas-cost-usage-exporter/Dockerfile, atlas-cost-usage-exporter/docker-compose.yml, github-db-driver-version-exporter/Dockerfile, github-db-driver-version-exporter/docker-compose.yml, mongodb-atlas-api/Dockerfile, mongodb-atlas-api/docker-compose.yaml, mongodb-version-tracking-exporter/Dockerfile, mongodb-version-tracking-exporter/docker-compose.yaml
- **Kubernetes Helm:** chart/atlas-cost-gcs-exporter/Chart.yaml, chart/atlas-cost-usage-exporter/Chart.yaml, chart/github-db-driver-version-exporter/Chart.yaml, chart/mongodb-atlas-api/Chart.yaml, chart/mongodb-version-tracking-exporter/Chart.yaml
- **Terraform:** terraform/modules/atlas-cost-gcs-exporter/iam.tf, terraform/modules/atlas-cost-gcs-exporter/main.tf, terraform/modules/atlas-cost-gcs-exporter/variables.tf, terraform/modules/atlas-cost-usage-exporter/iam.tf, terraform/modules/atlas-cost-usage-exporter/main.tf, terraform/modules/atlas-cost-usage-exporter/variables.tf, terraform/modules/github-db-driver-version-exporter/iam.tf, terraform/modules/github-db-driver-version-exporter/main.tf, terraform/modules/github-db-driver-version-exporter/s3.tf, terraform/modules/github-db-driver-version-exporter/variables.tf, terraform/modules/mongodb-atlas-api/iam.tf, terraform/modules/mongodb-atlas-api/main.tf, terraform/modules/mongodb-atlas-api/variables.tf, terraform/modules/mongodb-version-tracking-exporter/iam.tf, terraform/modules/mongodb-version-tracking-exporter/main.tf, terraform/modules/mongodb-version-tracking-exporter/variables.tf, terraform/phases/atlas-cost-gcs-exporter-dev/main.tf, terraform/phases/atlas-cost-gcs-exporter-dev/variables.tf, terraform/phases/atlas-cost-gcs-exporter-prod/main.tf, terraform/phases/atlas-cost-gcs-exporter-prod/variables.tf, terraform/phases/atlas-cost-usage-exporter-dev/main.tf, terraform/phases/atlas-cost-usage-exporter-dev/variables.tf, terraform/phases/atlas-cost-usage-exporter-prod/main.tf, terraform/phases/atlas-cost-usage-exporter-prod/variables.tf, terraform/phases/github-db-driver-version-exporter-dev/main.tf, terraform/phases/github-db-driver-version-exporter-dev/variables.tf, terraform/phases/github-db-driver-version-exporter-prod/main.tf, terraform/phases/github-db-driver-version-exporter-prod/variables.tf, terraform/phases/mongodb-atlas-api-dev/main.tf, terraform/phases/mongodb-atlas-api-dev/variables.tf, terraform/phases/mongodb-atlas-api-prod/main.tf, terraform/phases/mongodb-atlas-api-prod/variables.tf, terraform/phases/mongodb-version-tracking-exporter-dev/main.tf, terraform/phases/mongodb-version-tracking-exporter-dev/variables.tf, terraform/phases/mongodb-version-tracking-exporter-prod/main.tf, terraform/phases/mongodb-version-tracking-exporter-prod/variables.tf
- **Ci Cd:** .github/workflows/build-atlas-cost-gcs-exporter.yaml, .github/workflows/build-atlas-cost-usage-exporter.yaml, .github/workflows/build-github-db-driver-version-exporter.yaml, .github/workflows/build-mongodb-atlas-api.yaml, .github/workflows/build-mongodb-atlas-exporter.yaml, .github/workflows/build-mongodb-github-driver-version-exporter.yaml, .github/workflows/build-mongodb-version-tracking-exporter.yaml, .github/workflows/go-unit-test.yaml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/pr-reviews.yaml, .github/workflows/pr-title-validation.yaml, .github/workflows/set-self.yaml, .github/workflows/setup-repository.yaml
- **Api Specs:** Not detected
- **Documentation:** README.md

## 4. Main Components and Code Structure

### chart
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 65 analyzed core files under chart/

### terraform
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 51 analyzed core files under terraform/

### mongodb-atlas-api
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 25 analyzed core files under mongodb-atlas-api/

### .github
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 16 analyzed core files under .github/

### atlas-cost-usage-exporter
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 11 analyzed core files under atlas-cost-usage-exporter/

### atlas-cost-gcs-exporter
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 6 analyzed core files under atlas-cost-gcs-exporter/

### mongodb-version-tracking-exporter
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 4 analyzed core files under mongodb-version-tracking-exporter/

### github-db-driver-version-exporter
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 4 analyzed core files under github-db-driver-version-exporter/

### ci
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 2 analyzed core files under ci/

## 5. Code Architecture

- **Architecture Style:** Modular Python application architecture
- **Architecture Explanation:** The repository follows a modular python application architecture. Static analysis identified 9 major structural component areas, 6 executable/package entry points, and 0 repository-local dependency relationships. The architecture below is generated from source layout, imports, symbols, package metadata and executable entry points; the local LLM is used only to explain these facts in repository-specific language.

### Layers / Modules

| Layer / Module | Description | Evidence |
| --- | --- | --- |
| chart | Top-level source/component area; semantic responsibility refined by local LLM | 65 analyzed core files under chart/ |
| terraform | Top-level source/component area; semantic responsibility refined by local LLM | 51 analyzed core files under terraform/ |
| mongodb-atlas-api | Top-level source/component area; semantic responsibility refined by local LLM | 25 analyzed core files under mongodb-atlas-api/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 16 analyzed core files under .github/ |
| atlas-cost-usage-exporter | Top-level source/component area; semantic responsibility refined by local LLM | 11 analyzed core files under atlas-cost-usage-exporter/ |
| atlas-cost-gcs-exporter | Top-level source/component area; semantic responsibility refined by local LLM | 6 analyzed core files under atlas-cost-gcs-exporter/ |
| mongodb-version-tracking-exporter | Top-level source/component area; semantic responsibility refined by local LLM | 4 analyzed core files under mongodb-version-tracking-exporter/ |
| github-db-driver-version-exporter | Top-level source/component area; semantic responsibility refined by local LLM | 4 analyzed core files under github-db-driver-version-exporter/ |
| ci | Top-level source/component area; semantic responsibility refined by local LLM | 2 analyzed core files under ci/ |

### Entry Points

| Type | Symbol / Command | Source File |
| --- | --- | --- |
| Python executable entry point | mongodb-version-tracking-exporter.main | mongodb-version-tracking-exporter/main.py |
| Python executable entry point | atlas-cost-gcs-exporter.atlas_cost_gcs_cluster_proposition_org | atlas-cost-gcs-exporter/atlas_cost_gcs_cluster_proposition_org.py |
| Python executable entry point | atlas-cost-gcs-exporter.export_csv | atlas-cost-gcs-exporter/export_csv.py |
| Python executable entry point | github-db-driver-version-exporter.github_multi_engine_dbdriver_compat_exporter | github-db-driver-version-exporter/github_multi_engine_dbdriver_compat_exporter.py |
| Go executable entry point | mongodb-atlas-api:main | mongodb-atlas-api/main.go |
| Go executable entry point | atlas-cost-usage-exporter:main | atlas-cost-usage-exporter/main.go |

### Major Components

| Component | Responsibility | Evidence |
| --- | --- | --- |
| chart | Top-level source/component area; semantic responsibility refined by local LLM | 65 analyzed core files under chart/ |
| terraform | Top-level source/component area; semantic responsibility refined by local LLM | 51 analyzed core files under terraform/ |
| mongodb-atlas-api | Top-level source/component area; semantic responsibility refined by local LLM | 25 analyzed core files under mongodb-atlas-api/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 16 analyzed core files under .github/ |
| atlas-cost-usage-exporter | Top-level source/component area; semantic responsibility refined by local LLM | 11 analyzed core files under atlas-cost-usage-exporter/ |
| atlas-cost-gcs-exporter | Top-level source/component area; semantic responsibility refined by local LLM | 6 analyzed core files under atlas-cost-gcs-exporter/ |
| mongodb-version-tracking-exporter | Top-level source/component area; semantic responsibility refined by local LLM | 4 analyzed core files under mongodb-version-tracking-exporter/ |
| github-db-driver-version-exporter | Top-level source/component area; semantic responsibility refined by local LLM | 4 analyzed core files under github-db-driver-version-exporter/ |
| ci | Top-level source/component area; semantic responsibility refined by local LLM | 2 analyzed core files under ci/ |

### Component Relationships

_Not detected._

### Configuration Model

Repository contains explicit configuration artifacts: atlas-cost-usage-exporter/config.yaml, mongodb-atlas-api/config.yaml.

### Extension Points

No explicit extension points were statically identified.

### Deployment Model

Docker, Kubernetes/Helm, Terraform-managed infrastructure

### Architecture Data / Control Flow

1. Execution begins at the detected repository entry point(s): mongodb-version-tracking-exporter/main.py, atlas-cost-gcs-exporter/atlas_cost_gcs_cluster_proposition_org.py, atlas-cost-gcs-exporter/export_csv.py, github-db-driver-version-exporter/github_multi_engine_dbdriver_compat_exporter.py, mongodb-atlas-api/main.go, atlas-cost-usage-exporter/main.go.
2. Static call/import analysis identified concrete execution paths shown in Detailed Code Flows below.
3. Configuration artifacts influence component initialization and runtime behavior.
4. Core components process requests/commands/events through repository modules and return results to the caller or downstream integration.

## 6. Overall Code Flow

- **Code Flow Analysis Status:** Deterministic static code-flow fallback (--skip-llm)

This section explains the repository flow in simple execution order. It separates the main runtime from independent automation/tooling paths and only uses code/source evidence found in the repository.

### Flow Overview

The repository runtime starts from its executable entry point, loads configuration and infrastructure dependencies, registers production routes, and starts the service. Each request then follows the statically resolved handler -> use case/service -> repository -> DAL/client path where such a chain is proven. Persistence operations are shown only when directly detected in source. The service closes through its graceful shutdown path when one is present.

### Application Startup Flow

#### Step 1: Start the application

Execution starts in mongodb-atlas-api/main.go at main. The startup function then delegates into the application bootstrap code shown below.

**Code / files involved:**
- `mongodb-atlas-api/main.go:main`
- `prom.StartMetricServer`
- `utils.GetConfig`
- `atlas.NewAtlasClient`
- `report.NewCollector`
- `tasks.NewAutoPause`
- `tasks.NewBackup`
- `tasks.NewInventory`
- `tasks.NewLogs`

**What happens next:** Control moves into application initialization.

**Evidence:** mongodb-atlas-api/main.go

#### Step 2: Load runtime configuration

The application uses the detected configuration files during startup. Configuration values control later runtime initialization; values not proven from source are not guessed.

**Code / files involved:**
- `atlas-cost-usage-exporter/config.yaml`
- `mongodb-atlas-api/config.yaml`

**What happens next:** Validated runtime settings are available to the bootstrap code.

**Evidence:** atlas-cost-usage-exporter/config.yaml, mongodb-atlas-api/config.yaml

#### Step 3: Build application dependencies and start the server

The main bootstrap creates the runtime dependencies in code order. The detected calls include logging/metrics setup, database/client connection, repository/use-case/handler construction, HTTP server creation and service start where present.

**Code / files involved:**
- `atlas-cost-usage-exporter/main.go:main`
- `billing.Schedule`
- `collector.StartWebServer`
- `GetConfig`
- `NewClient`
- `NewCollector`
- `NewBillingTask`

**What happens next:** The service is initialized and ready to receive runtime work.

**Evidence:** atlas-cost-usage-exporter/main.go

### Static Call / Module Paths

The paths below are the exact callable/import chains that static analysis could prove. They support the simplified flow above.

#### Python control flow from main
- **Entry Point:** mongodb-version-tracking-exporter.main.main
- **Ordered Static Flow:**
  1. `mongodb-version-tracking-exporter.main.main`
  2. `mongodb-version-tracking-exporter.main.get_all_projects`
  3. `mongodb-version-tracking-exporter.main._http_get`
- **Evidence:** Static AST self/local function call graph

#### Python control flow from main
- **Entry Point:** atlas-cost-gcs-exporter.atlas_cost_gcs_cluster_proposition_org.main
- **Ordered Static Flow:**
  1. `atlas-cost-gcs-exporter.atlas_cost_gcs_cluster_proposition_org.main`
  2. `atlas-cost-gcs-exporter.atlas_cost_gcs_cluster_proposition_org.process_org_cost`
  3. `atlas-cost-gcs-exporter.atlas_cost_gcs_cluster_proposition_org.flatten_usage`
- **Evidence:** Static AST self/local function call graph

#### Python control flow from download_invoices_as_csv
- **Entry Point:** atlas-cost-gcs-exporter.export_csv.download_invoices_as_csv
- **Ordered Static Flow:**
  1. `atlas-cost-gcs-exporter.export_csv.download_invoices_as_csv`
  2. `atlas-cost-gcs-exporter.export_csv.fetch_single_invoice`
  3. `atlas-cost-gcs-exporter.export_csv.with_retries`
- **Evidence:** Static AST self/local function call graph

#### Python control flow from main
- **Entry Point:** atlas-cost-gcs-exporter.export_csv.main
- **Ordered Static Flow:**
  1. `atlas-cost-gcs-exporter.export_csv.main`
  2. `atlas-cost-gcs-exporter.export_csv.load_environment`
- **Evidence:** Static AST self/local function call graph

## 7. Dependencies and Compatibility

Dependencies are grouped by scope. Example/test/documentation dependencies do not contaminate the core technology stack.

### Core Dependencies

| Dependency | Current Version / Constraint | Source | Latest Version | Compatibility | Notes |
| --- | --- | --- | --- | --- | --- |
| github.com/beorn7/perks | v1.0.1 | mongodb-atlas-api/go.mod | v1.0.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/beorn7/perks |
| github.com/cespare/xxhash/v2 | v2.2.0 | mongodb-atlas-api/go.mod | v2.3.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/cespare/xxhash/v2 |
| github.com/davecgh/go-spew | v1.1.1 | mongodb-atlas-api/go.mod | v1.1.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/davecgh/go-spew |
| github.com/go-co-op/gocron | v1.30.1 | mongodb-atlas-api/go.mod | v1.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-co-op/gocron |
| github.com/golang/protobuf | v1.5.3 | mongodb-atlas-api/go.mod | v1.5.4 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/golang/protobuf |
| github.com/golang/snappy | v0.0.4 | mongodb-atlas-api/go.mod | v1.0.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/golang/snappy |
| github.com/google/uuid | v1.4.0 | atlas-cost-usage-exporter/go.mod | v1.6.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/google/uuid |
| github.com/klauspost/compress | v1.16.7 | mongodb-atlas-api/go.mod | v1.20.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/klauspost/compress |
| github.com/matttproud/golang_protobuf_extensions | v1.0.4 | mongodb-atlas-api/go.mod | v1.0.4 | CURRENT | Latest version source: https://pkg.go.dev/github.com/matttproud/golang_protobuf_extensions |
| github.com/mongodb-forks/digest | v1.1.0 | mongodb-atlas-api/go.mod | v1.1.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/mongodb-forks/digest |
| github.com/mongodb-forks/digest | v1.1.0 | atlas-cost-usage-exporter/go.mod | v1.1.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/mongodb-forks/digest |
| github.com/montanaflynn/stats | v0.7.1 | mongodb-atlas-api/go.mod | v0.12.6 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/montanaflynn/stats |
| github.com/pmezard/go-difflib | v1.0.0 | mongodb-atlas-api/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/pmezard/go-difflib |
| github.com/prometheus/client_golang | v1.16.0 | mongodb-atlas-api/go.mod | v1.24.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/client_golang |
| github.com/prometheus/client_model | v0.3.0 | mongodb-atlas-api/go.mod | v0.6.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/client_model |
| github.com/prometheus/common | v0.42.0 | mongodb-atlas-api/go.mod | v0.71.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/common |
| github.com/prometheus/procfs | v0.10.1 | mongodb-atlas-api/go.mod | v0.22.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/procfs |
| github.com/robfig/cron/v3 | v3.0.1 | mongodb-atlas-api/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/robfig/cron/v3 |
| github.com/robfig/cron/v3 | v3.0.1 | atlas-cost-usage-exporter/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/robfig/cron/v3 |
| github.com/stretchr/objx | v0.5.2 | mongodb-atlas-api/go.mod | v0.5.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/stretchr/objx |
| github.com/stretchr/testify | v1.9.0 | mongodb-atlas-api/go.mod | v1.12.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/stretchr/testify |
| github.com/xdg-go/pbkdf2 | v1.0.0 | mongodb-atlas-api/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/xdg-go/pbkdf2 |
| github.com/xdg-go/scram | v1.1.2 | mongodb-atlas-api/go.mod | v1.2.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/xdg-go/scram |
| github.com/xdg-go/stringprep | v1.0.4 | mongodb-atlas-api/go.mod | v1.0.4 | CURRENT | Latest version source: https://pkg.go.dev/github.com/xdg-go/stringprep |
| github.com/youmark/pkcs8 | v0.0.0-20240726163527-a2c0da244d78 | mongodb-atlas-api/go.mod | v0.0.0-20240726163527-a2c0da244d78 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/youmark/pkcs8 |
| go.mongodb.org/atlas-sdk/v20240805004 | v20240805004.7.0 | mongodb-atlas-api/go.mod | v20240805004.7.0 | CURRENT | Latest version source: https://pkg.go.dev/go.mongodb.org/atlas-sdk/v20240805004 |
| go.mongodb.org/atlas-sdk/v20240805004 | v20240805004.7.0 | atlas-cost-usage-exporter/go.mod | v20240805004.7.0 | CURRENT | Latest version source: https://pkg.go.dev/go.mongodb.org/atlas-sdk/v20240805004 |
| go.mongodb.org/mongo-driver | v1.17.9 | mongodb-atlas-api/go.mod | v1.17.10 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.mongodb.org/mongo-driver |
| go.uber.org/atomic | v1.9.0 | mongodb-atlas-api/go.mod | v1.12.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.uber.org/atomic |
| go.uber.org/atomic | v1.9.0 | atlas-cost-usage-exporter/go.mod | v1.12.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.uber.org/atomic |
| golang.org/x/crypto | v0.26.0 | mongodb-atlas-api/go.mod | v0.57.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/crypto |
| golang.org/x/sync | v0.8.0 | mongodb-atlas-api/go.mod | v0.23.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/sync |
| golang.org/x/sys | v0.23.0 | mongodb-atlas-api/go.mod | v0.48.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/sys |
| golang.org/x/text | v0.17.0 | mongodb-atlas-api/go.mod | v0.42.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/text |
| google-cloud-storage | >=2.14.0 | atlas-cost-gcs-exporter/requirements.txt | 3.14.1 | UNKNOWN | Latest version source: https://pypi.org/project/google-cloud-storage/ |
| google.golang.org/protobuf | v1.30.0 | mongodb-atlas-api/go.mod | v1.36.12 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/google.golang.org/protobuf |
| gopkg.in/yaml.v3 | v3.0.1 | mongodb-atlas-api/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v3 |
| gopkg.in/yaml.v3 | v3.0.1 | atlas-cost-usage-exporter/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v3 |
| python-dateutil | >=2.8.2 | atlas-cost-gcs-exporter/requirements.txt | 2.9.0.post0 | UNKNOWN | Latest version source: https://pypi.org/project/python-dateutil/ |
| python-dotenv | >=1.0.0 | atlas-cost-gcs-exporter/requirements.txt | 1.2.3 | UNKNOWN | Latest version source: https://pypi.org/project/python-dotenv/ |
| requests | >=2.31.0 | atlas-cost-gcs-exporter/requirements.txt | 2.34.2 | UNKNOWN | Latest version source: https://pypi.org/project/requests/ |

## 8. Tests and Coverage

- **Testing frameworks:** Testify
- **Test files detected:** 1
- **Coverage status:** Actual coverage result not found
- **Coverage percentage:** Not available
- **Coverage source:** Not available

## 9. Production Internal APIs

_Test/mock/example routes are excluded._

| Method | Endpoint | Handler | Component | Source File |
| --- | --- | --- | --- | --- |
| ROUTE | /healthz | Not available | server | atlas-cost-usage-exporter/server.go |
| ROUTE | /api/v1/reports/organizations | handleOrganizationsReport | server | atlas-cost-usage-exporter/server.go |
| ROUTE | /api/v1/reports/projects | handleProjectsReport | server | atlas-cost-usage-exporter/server.go |
| ROUTE | /api/v1/status | Not available | server | atlas-cost-usage-exporter/server.go |
| GET | from | Not available | server | atlas-cost-usage-exporter/server.go |
| GET | to | Not available | server | atlas-cost-usage-exporter/server.go |
| GET | https://api64.ipify.org | Not available | atlas_exporter | mongodb-atlas-api/tasks/atlas_exporter.go |
| ROUTE | /metrics | Not available | prometheus | mongodb-atlas-api/utils/prom/prometheus.go |
| ROUTE | /autopause | Not available | report | mongodb-atlas-api/utils/report/report.go |
| ROUTE | /clusters | Not available | report | mongodb-atlas-api/utils/report/report.go |
| ROUTE | /atlas-exporter | Not available | report | mongodb-atlas-api/utils/report/report.go |
| ROUTE | /healthz | Not available | report | mongodb-atlas-api/utils/report/report.go |

## 10. Production External API and Integration Calls

_Test/mock/example calls are excluded._

| Caller | Technology | Target | Method | Source File | Evidence |
| --- | --- | --- | --- | --- | --- |
| main | requests | Not available | GET | mongodb-version-tracking-exporter/main.py | Detected requests.get |
| main | requests | Not available | POST | mongodb-version-tracking-exporter/main.py | Detected requests.post |
| atlas_cost_gcs_cluster_proposition_org | requests | Not available | POST | atlas-cost-gcs-exporter/atlas_cost_gcs_cluster_proposition_org.py | Detected requests.post |
| atlas_cost_gcs_cluster_proposition_org | requests | Not available | GET | atlas-cost-gcs-exporter/atlas_cost_gcs_cluster_proposition_org.py | Detected requests.get |
| export_csv | requests | Not available | GET | atlas-cost-gcs-exporter/export_csv.py | Detected requests.get |
| github_multi_engine_dbdriver_compat_exporter | requests | Not available | SESSION | github-db-driver-version-exporter/github_multi_engine_dbdriver_compat_exporter.py | Detected requests.Session |
| github_multi_engine_dbdriver_compat_exporter | AWS SDK (boto3) | s3 | client | github-db-driver-version-exporter/github_multi_engine_dbdriver_compat_exporter.py | Detected boto3.client |
| github_multi_engine_dbdriver_compat_exporter | requests | Not available | PUT | github-db-driver-version-exporter/github_multi_engine_dbdriver_compat_exporter.py | Detected requests.put |
| github_multi_engine_dbdriver_compat_exporter | requests | Not available | POST | github-db-driver-version-exporter/github_multi_engine_dbdriver_compat_exporter.py | Detected requests.post |
| github_multi_engine_dbdriver_compat_exporter | requests | Not available | HTTPERROR | github-db-driver-version-exporter/github_multi_engine_dbdriver_compat_exporter.py | Detected requests.HTTPError |
| logs | Go net/http | url | POST | mongodb-atlas-api/tasks/logs.go | http.NewRequest call |

## 11. Main Use Cases

No high-level use cases were returned by the local LLM.

## 12. Analysis Limitations

- Local LLM skipped; deterministic architecture and detailed static code flow are still reported.
