# Repository Intelligent Analysis Report

## 1. Repository Summary

- **Repository:** cloud-resource-scanner-src
- **Source:** https://github.com/NBCUDTC/cloud-resource-scanner-src.git
- **Source Type:** GitHub
- **Repository Type:** Application / Service / Library Repository
- **Files Analyzed:** 160
- **Local LLM Status:** Skipped by command line

### What the Application / Repository Does

Main wiki with business description and objectives. The Cloud Resource Scanner consolidates information from multiple AWS accounts and GCP projects into Prometheus metrics for alerting and dashboarding. From AWS accounts, it scans IAM keys, NAT Gateway IP addresses, and certificate expiration dates. From GCP projects, it scans IAM keys and certificate expiration dates. The Cloud Resource Scanner is responsible for the data behind these 3 dashboards: 1. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/certificate-inventory 2. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/ip-inventory 3. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/user-key-inventory 4. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/compliance-summary The Cloud Resource Scanner runs using the arn:aws:iam::608746997981:role/cloud-resource-scanner IAM Role. Each AWS account needs to create a role that can be assumed by the Cloud Resource Scanner role. AWS IAM Roles for the CRS can be found here. Terraform to create that role is:

### Repository Summary

Main wiki with business description and objectives. The Cloud Resource Scanner consolidates information from multiple AWS accounts and GCP projects into Prometheus metrics for alerting and dashboarding. From AWS accounts, it scans IAM keys, NAT Gateway IP addresses, and certificate expiration dates. From GCP projects, it scans IAM keys and certificate expiration dates. The Cloud Resource Scanner is responsible for the data behind these 3 dashboards: 1. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/certificate-inventory 2. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/ip-inventory 3. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/user-key-inventory 4. https://prod-grafana-us-east-2.helios-prod.nbcuni.com/d/compliance-summary The Cloud Resource Scanner runs using the arn:aws:iam::608746997981:role/cloud-resource-scanner IAM Role. Each AWS account needs to create a role that can be assumed by the Cloud Resource Scanner role. AWS IAM Roles for the CRS can be found here. Terraform to create that role is:

## 2. Technology Stack

- **Languages:** Go, Terraform
- **Frameworks:** Not detected
- **Runtime:** Go 1.26.4
- **Databases:** Not detected
- **Cloud Platforms:** Not detected
- **Containers:** Docker, Docker Compose
- **Kubernetes Helm Terraform:** Helm, Terraform
- **Ci Cd:** GitHub Actions
- **Testing Tools:** Testify
- **Monitoring Observability:** Prometheus
- **Important Core Libraries:** cel.dev/expr, cloud.google.com/go, cloud.google.com/go/auth, cloud.google.com/go/auth/oauth2adapt, cloud.google.com/go/compute, cloud.google.com/go/compute/metadata, cloud.google.com/go/iam, cloud.google.com/go/monitoring, cloud.google.com/go/storage, github.com/99designs/go-keychain, github.com/99designs/keyring, github.com/akamai/akamaiopen-edgegrid-golang/v4, github.com/andybalholm/brotli, github.com/apache/arrow-go/v18, github.com/apache/thrift, github.com/apex/log, github.com/aws/aws-sdk-go, github.com/aws/aws-sdk-go-v2, github.com/aws/aws-sdk-go-v2/aws/protocol/eventstream, github.com/aws/aws-sdk-go-v2/config, github.com/aws/aws-sdk-go-v2/credentials, github.com/aws/aws-sdk-go-v2/feature/ec2/imds, github.com/aws/aws-sdk-go-v2/feature/s3/manager, github.com/aws/aws-sdk-go-v2/internal/configsources, github.com/aws/aws-sdk-go-v2/internal/endpoints/v2, github.com/aws/aws-sdk-go-v2/internal/ini, github.com/aws/aws-sdk-go-v2/internal/v4a, github.com/aws/aws-sdk-go-v2/service/internal/accept-encoding, github.com/aws/aws-sdk-go-v2/service/internal/checksum, github.com/aws/aws-sdk-go-v2/service/internal/presigned-url, github.com/aws/aws-sdk-go-v2/service/internal/s3shared, github.com/aws/aws-sdk-go-v2/service/s3, github.com/aws/aws-sdk-go-v2/service/sso, github.com/aws/aws-sdk-go-v2/service/ssooidc, github.com/aws/aws-sdk-go-v2/service/sts, github.com/aws/smithy-go, github.com/azure/azure-sdk-for-go/sdk/azcore, github.com/azure/azure-sdk-for-go/sdk/internal, github.com/azure/azure-sdk-for-go/sdk/storage/azblob, github.com/beorn7/perks, github.com/burntsushi/toml, github.com/cespare/xxhash/v2, github.com/cncf/xds/go, github.com/danieljoos/wincred, github.com/davecgh/go-spew, github.com/dvsekhvalnov/jose2go, github.com/emicklei/go-restful/v3, github.com/envoyproxy/go-control-plane/envoy, github.com/envoyproxy/protoc-gen-validate, github.com/fastly/go-fastly/v6, github.com/felixge/httpsnoop, github.com/fxamacker/cbor/v2, github.com/gabriel-vasile/mimetype, github.com/go-co-op/gocron, github.com/go-jose/go-jose/v4, github.com/go-logr/logr, github.com/go-logr/stdr, github.com/go-openapi/jsonpointer, github.com/go-openapi/jsonreference, github.com/go-openapi/swag, github.com/go-openapi/swag/cmdutils, github.com/go-openapi/swag/conv, github.com/go-openapi/swag/fileutils, github.com/go-openapi/swag/jsonname, github.com/go-openapi/swag/jsonutils, github.com/go-openapi/swag/loading, github.com/go-openapi/swag/mangling, github.com/go-openapi/swag/netutils, github.com/go-openapi/swag/stringutils, github.com/go-openapi/swag/typeutils, github.com/go-openapi/swag/yamlutils, github.com/goccy/go-json, github.com/godbus/dbus, github.com/gogo/protobuf, github.com/golang-jwt/jwt/v5, github.com/golang/protobuf, github.com/golang/snappy, github.com/google/flatbuffers, github.com/google/gnostic-models, github.com/google/go-cmp

## 3. Repository Scan and Engineering Artifacts

- **Important files:** .github/workflows/build.yaml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/pr-reviews.yaml, .github/workflows/pr-title-validation.yaml, .github/workflows/set-self.yaml, .github/workflows/setup-repository.yaml, README.md

- **Configuration:** .env.example, src/.env.example, src/config.yaml, src/utils/config/main.go, src/utils/config/main_test.go
- **Docker:** docker-compose.yaml, src/Dockerfile
- **Kubernetes Helm:** chart/Chart.yaml
- **Terraform:** terraform/modules/cloud-resource-scanner/iam.tf, terraform/modules/cloud-resource-scanner/main.tf, terraform/modules/cloud-resource-scanner/sg.tf, terraform/modules/cloud-resource-scanner/variables.tf, terraform/phases/dev/main.tf, terraform/phases/dev/secrets.tf, terraform/phases/dev/variables.tf, terraform/phases/int-nft/main.tf, terraform/phases/int-nft/secrets.tf, terraform/phases/int-nft/variables.tf, terraform/phases/int/main.tf, terraform/phases/int/secrets.tf, terraform/phases/int/variables.tf, terraform/phases/prod-new/main.tf, terraform/phases/prod-new/secrets.tf, terraform/phases/prod-new/variables.tf, terraform/phases/prod/main.tf, terraform/phases/prod/secrets.tf, terraform/phases/prod/variables.tf, terraform/phases/stage/main.tf, terraform/phases/stage/secrets.tf, terraform/phases/stage/variables.tf
- **Ci Cd:** .github/workflows/build.yaml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/pr-reviews.yaml, .github/workflows/pr-title-validation.yaml, .github/workflows/set-self.yaml, .github/workflows/setup-repository.yaml
- **Api Specs:** Not detected
- **Documentation:** README.md, docs/designs/template.md, docs/snowflake-saml-certs-setup.sql

## 4. Main Components and Code Structure

### src
Primary source implementation
**Evidence:** 66 analyzed core files under src/

### chart
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 43 analyzed core files under chart/

### terraform
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 29 analyzed core files under terraform/

### .github
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 10 analyzed core files under .github/

### ci
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 4 analyzed core files under ci/

## 5. Code Architecture

- **Architecture Style:** Modular repository architecture
- **Architecture Explanation:** The repository follows a modular repository architecture. Static analysis identified 5 major structural component areas, 1 executable/package entry points, and 0 repository-local dependency relationships. The architecture below is generated from source layout, imports, symbols, package metadata and executable entry points; the local LLM is used only to explain these facts in repository-specific language.

### Layers / Modules

| Layer / Module | Description | Evidence |
| --- | --- | --- |
| src | Primary source implementation | 66 analyzed core files under src/ |
| chart | Top-level source/component area; semantic responsibility refined by local LLM | 43 analyzed core files under chart/ |
| terraform | Top-level source/component area; semantic responsibility refined by local LLM | 29 analyzed core files under terraform/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under .github/ |
| ci | Top-level source/component area; semantic responsibility refined by local LLM | 4 analyzed core files under ci/ |

### Entry Points

| Type | Symbol / Command | Source File |
| --- | --- | --- |
| Go executable entry point | src:main | src/main.go |

### Major Components

| Component | Responsibility | Evidence |
| --- | --- | --- |
| src | Primary source implementation | 66 analyzed core files under src/ |
| chart | Top-level source/component area; semantic responsibility refined by local LLM | 43 analyzed core files under chart/ |
| terraform | Top-level source/component area; semantic responsibility refined by local LLM | 29 analyzed core files under terraform/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under .github/ |
| ci | Top-level source/component area; semantic responsibility refined by local LLM | 4 analyzed core files under ci/ |

### Component Relationships

_Not detected._

### Configuration Model

Repository contains explicit configuration artifacts: .env.example, src/.env.example, src/config.yaml, src/utils/config/main.go, src/utils/config/main_test.go.

### Extension Points

No explicit extension points were statically identified.

### Deployment Model

Docker, Kubernetes/Helm, Terraform-managed infrastructure

### Architecture Data / Control Flow

1. Execution begins at the detected repository entry point(s): src/main.go.
2. Configuration artifacts influence component initialization and runtime behavior.
3. Core components process requests/commands/events through repository modules and return results to the caller or downstream integration.

## 6. Overall Code Flow

- **Code Flow Analysis Status:** Deterministic static code-flow fallback (--skip-llm)

This section explains the repository flow in simple execution order. It separates the main runtime from independent automation/tooling paths and only uses code/source evidence found in the repository.

### Flow Overview

The repository runtime starts from its executable entry point, loads configuration and infrastructure dependencies, registers production routes, and starts the service. Each request then follows the statically resolved handler -> use case/service -> repository -> DAL/client path where such a chain is proven. Persistence operations are shown only when directly detected in source. The service closes through its graceful shutdown path when one is present.

### Application Startup Flow

#### Step 1: Start the application

Execution starts in src/main.go at main. The startup function then delegates into the application bootstrap code shown below.

**Code / files involved:**
- `src/main.go:main`
- `logging.Init`
- `config.Init`
- `metrics.StartServer`
- `public.StartServer`
- `private.StartServer`
- `executeProgram`

**What happens next:** Control moves into application initialization.

**Evidence:** src/main.go

#### Step 2: Load runtime configuration

The application uses the detected configuration files during startup. Configuration values control later runtime initialization; values not proven from source are not guessed.

**Code / files involved:**
- `.env.example`
- `src/.env.example`
- `src/config.yaml`
- `src/utils/config/main.go`
- `src/utils/config/main_test.go`

**What happens next:** Validated runtime settings are available to the bootstrap code.

**Evidence:** .env.example, src/.env.example, src/config.yaml, src/utils/config/main.go, src/utils/config/main_test.go

### Static Call / Module Paths

The paths below are the exact callable/import chains that static analysis could prove. They support the simplified flow above.

No complete callable chain was statically provable for this repository.

## 7. Dependencies and Compatibility

Dependencies are grouped by scope. Example/test/documentation dependencies do not contaminate the core technology stack.

### Core Dependencies

| Dependency | Current Version / Constraint | Source | Latest Version | Compatibility | Notes |
| --- | --- | --- | --- | --- | --- |
| cel.dev/expr | v0.25.2 | src/go.mod | v0.25.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/cel.dev/expr |
| cloud.google.com/go | v0.123.0 | src/go.mod | v0.123.0 | CURRENT | Latest version source: https://pkg.go.dev/cloud.google.com/go |
| cloud.google.com/go/auth | v0.20.0 | src/go.mod | v0.23.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/cloud.google.com/go/auth |
| cloud.google.com/go/auth/oauth2adapt | v0.2.8 | src/go.mod | v0.2.8 | CURRENT | Latest version source: https://pkg.go.dev/cloud.google.com/go/auth/oauth2adapt |
| cloud.google.com/go/compute | v1.64.0 | src/go.mod | v1.69.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/cloud.google.com/go/compute |
| cloud.google.com/go/compute/metadata | v0.9.0 | src/go.mod | v0.9.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/cloud.google.com/go/compute/metadata |
| cloud.google.com/go/iam | v1.11.0 | src/go.mod | v1.13.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/cloud.google.com/go/iam |
| cloud.google.com/go/monitoring | v1.29.0 | src/go.mod | v1.30.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/cloud.google.com/go/monitoring |
| cloud.google.com/go/storage | v1.56.3 | src/go.mod | v1.68.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/cloud.google.com/go/storage |
| github.com/99designs/go-keychain | v0.0.0-20191008050251-8e49817e8af4 | src/go.mod | v0.0.0-20160105221929-9cf53c87839c | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/99designs/go-keychain |
| github.com/99designs/keyring | v1.2.2 | src/go.mod | v1.2.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/99designs/keyring |
| github.com/akamai/AkamaiOPEN-edgegrid-golang/v4 | v4.1.0 | src/go.mod | v4.1.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/akamai/AkamaiOPEN-edgegrid-golang/v4 |
| github.com/andybalholm/brotli | v1.2.0 | src/go.mod | v1.2.4 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/andybalholm/brotli |
| github.com/apache/arrow-go/v18 | v18.4.0 | src/go.mod | v18.8.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/apache/arrow-go/v18 |
| github.com/apache/thrift | v0.22.0 | src/go.mod | v0.24.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/apache/thrift |
| github.com/apex/log | v1.9.0 | src/go.mod | v1.9.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/apex/log |
| github.com/aws/aws-sdk-go | v1.55.8 | src/go.mod | v1.55.8 | CURRENT | Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go |
| github.com/aws/aws-sdk-go-v2 | v1.38.1 | src/go.mod | v1.47.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2 |
| github.com/aws/aws-sdk-go-v2/aws/protocol/eventstream | v1.6.2 | src/go.mod | v1.7.20 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/aws/protocol/eventstream |
| github.com/aws/aws-sdk-go-v2/config | v1.27.11 | src/go.mod | v1.33.5 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/config |
| github.com/aws/aws-sdk-go-v2/credentials | v1.17.11 | src/go.mod | v1.20.5 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/credentials |
| github.com/aws/aws-sdk-go-v2/feature/ec2/imds | v1.16.1 | src/go.mod | v1.20.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/feature/ec2/imds |
| github.com/aws/aws-sdk-go-v2/feature/s3/manager | v1.16.15 | src/go.mod | v1.23.7 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/feature/s3/manager |
| github.com/aws/aws-sdk-go-v2/internal/configsources | v1.3.5 | src/go.mod | v1.5.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/internal/configsources |
| github.com/aws/aws-sdk-go-v2/internal/endpoints/v2 | v2.6.5 | src/go.mod | v2.8.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/internal/endpoints/v2 |
| github.com/aws/aws-sdk-go-v2/internal/ini | v1.8.0 | src/go.mod | v1.8.6 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/internal/ini |
| github.com/aws/aws-sdk-go-v2/internal/v4a | v1.3.5 | src/go.mod | v1.5.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/internal/v4a |
| github.com/aws/aws-sdk-go-v2/service/internal/accept-encoding | v1.11.2 | src/go.mod | v1.13.19 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/internal/accept-encoding |
| github.com/aws/aws-sdk-go-v2/service/internal/checksum | v1.3.7 | src/go.mod | v1.11.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/internal/checksum |
| github.com/aws/aws-sdk-go-v2/service/internal/presigned-url | v1.11.7 | src/go.mod | v1.14.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/internal/presigned-url |
| github.com/aws/aws-sdk-go-v2/service/internal/s3shared | v1.17.5 | src/go.mod | v1.20.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/internal/s3shared |
| github.com/aws/aws-sdk-go-v2/service/s3 | v1.53.1 | src/go.mod | v1.113.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/s3 |
| github.com/aws/aws-sdk-go-v2/service/sso | v1.20.5 | src/go.mod | v1.38.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/sso |
| github.com/aws/aws-sdk-go-v2/service/ssooidc | v1.23.4 | src/go.mod | v1.43.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/ssooidc |
| github.com/aws/aws-sdk-go-v2/service/sts | v1.28.6 | src/go.mod | v1.51.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/sts |
| github.com/aws/smithy-go | v1.22.5 | src/go.mod | v1.28.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/smithy-go |
| github.com/Azure/azure-sdk-for-go/sdk/azcore | v1.4.0 | src/go.mod | v1.23.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/Azure/azure-sdk-for-go/sdk/azcore |
| github.com/Azure/azure-sdk-for-go/sdk/internal | v1.1.2 | src/go.mod | v1.12.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/Azure/azure-sdk-for-go/sdk/internal |
| github.com/Azure/azure-sdk-for-go/sdk/storage/azblob | v1.0.0 | src/go.mod | v1.8.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/Azure/azure-sdk-for-go/sdk/storage/azblob |
| github.com/beorn7/perks | v1.0.1 | src/go.mod | v1.0.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/beorn7/perks |
| github.com/BurntSushi/toml | v1.4.0 | src/go.mod | v1.6.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/BurntSushi/toml |
| github.com/cespare/xxhash/v2 | v2.3.0 | src/go.mod | v2.3.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/cespare/xxhash/v2 |
| github.com/cncf/xds/go | v0.0.0-20260202195803-dba9d589def2 | src/go.mod | v0.0.0-20260202195803-dba9d589def2 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/cncf/xds/go |
| github.com/danieljoos/wincred | v1.2.2 | src/go.mod | v1.2.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/danieljoos/wincred |
| github.com/davecgh/go-spew | v1.1.2-0.20180830191138-d8f796af33cc | src/go.mod | v1.1.1 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/davecgh/go-spew |
| github.com/dvsekhvalnov/jose2go | v1.7.0 | src/go.mod | v1.11.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/dvsekhvalnov/jose2go |
| github.com/emicklei/go-restful/v3 | v3.13.0 | src/go.mod | v3.13.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/emicklei/go-restful/v3 |
| github.com/envoyproxy/go-control-plane/envoy | v1.37.0 | src/go.mod | v1.39.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/envoyproxy/go-control-plane/envoy |
| github.com/envoyproxy/protoc-gen-validate | v1.3.3 | src/go.mod | v1.3.3 | CURRENT | Latest version source: https://pkg.go.dev/github.com/envoyproxy/protoc-gen-validate |
| github.com/fastly/go-fastly/v6 | v6.8.0 | src/go.mod | v6.8.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/fastly/go-fastly/v6 |
| github.com/felixge/httpsnoop | v1.0.4 | src/go.mod | v1.1.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/felixge/httpsnoop |
| github.com/fxamacker/cbor/v2 | v2.7.1 | src/go.mod | v2.9.4 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/fxamacker/cbor/v2 |
| github.com/gabriel-vasile/mimetype | v1.4.7 | src/go.mod | v1.4.15 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/gabriel-vasile/mimetype |
| github.com/go-co-op/gocron | v1.37.0 | src/go.mod | v1.37.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/go-co-op/gocron |
| github.com/go-jose/go-jose/v4 | v4.1.4 | src/go.mod | v4.1.5 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-jose/go-jose/v4 |
| github.com/go-logr/logr | v1.4.3 | src/go.mod | v1.4.4 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-logr/logr |
| github.com/go-logr/stdr | v1.2.2 | src/go.mod | v1.2.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/go-logr/stdr |
| github.com/go-openapi/jsonpointer | v0.23.1 | src/go.mod | v1.0.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/jsonpointer |
| github.com/go-openapi/jsonreference | v0.21.6 | src/go.mod | v1.0.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/jsonreference |
| github.com/go-openapi/swag | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag |
| github.com/go-openapi/swag/cmdutils | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/cmdutils |
| github.com/go-openapi/swag/conv | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/conv |
| github.com/go-openapi/swag/fileutils | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/fileutils |
| github.com/go-openapi/swag/jsonname | v0.26.1 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/jsonname |
| github.com/go-openapi/swag/jsonutils | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/jsonutils |
| github.com/go-openapi/swag/loading | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/loading |
| github.com/go-openapi/swag/mangling | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/mangling |
| github.com/go-openapi/swag/netutils | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/netutils |
| github.com/go-openapi/swag/stringutils | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/stringutils |
| github.com/go-openapi/swag/typeutils | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/typeutils |
| github.com/go-openapi/swag/yamlutils | v0.25.5 | src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag/yamlutils |
| github.com/goccy/go-json | v0.10.5 | src/go.mod | v0.10.6 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/goccy/go-json |
| github.com/godbus/dbus | v0.0.0-20190726142602-4481cbc300e2 | src/go.mod | v4.1.0+incompatible | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/godbus/dbus |
| github.com/gogo/protobuf | v1.3.2 | src/go.mod | v1.3.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/gogo/protobuf |
| github.com/golang-jwt/jwt/v5 | v5.2.2 | src/go.mod | v5.3.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/golang-jwt/jwt/v5 |
| github.com/golang/protobuf | v1.5.4 | src/go.mod | v1.5.4 | CURRENT | Latest version source: https://pkg.go.dev/github.com/golang/protobuf |
| github.com/golang/snappy | v1.0.0 | src/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/golang/snappy |
| github.com/google/flatbuffers | v25.2.10+incompatible | src/go.mod | v25.12.19+incompatible | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/google/flatbuffers |
| github.com/google/gnostic-models | v0.6.9 | src/go.mod | v0.7.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/google/gnostic-models |
| github.com/google/go-cmp | v0.7.0 | src/go.mod | v0.7.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/google/go-cmp |
| github.com/google/go-querystring | v1.1.0 | src/go.mod | v1.2.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/google/go-querystring |
| github.com/google/gofuzz | v1.2.0 | src/go.mod | v1.2.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/google/gofuzz |
| github.com/google/jsonapi | v1.0.0 | src/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/google/jsonapi |
| github.com/google/s2a-go | v0.1.9 | src/go.mod | v0.1.10 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/google/s2a-go |
| github.com/google/uuid | v1.6.0 | src/go.mod | v1.6.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/google/uuid |
| github.com/googleapis/enterprise-certificate-proxy | v0.3.16 | src/go.mod | v0.3.22 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/googleapis/enterprise-certificate-proxy |
| github.com/googleapis/gax-go/v2 | v2.22.0 | src/go.mod | v2.24.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/googleapis/gax-go/v2 |
| github.com/GoogleCloudPlatform/opentelemetry-operations-go/detectors/gcp | v1.31.0 | src/go.mod | v1.38.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/GoogleCloudPlatform/opentelemetry-operations-go/detectors/gcp |
| github.com/GoogleCloudPlatform/opentelemetry-operations-go/exporter/metric | v0.53.0 | src/go.mod | v0.62.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/GoogleCloudPlatform/opentelemetry-operations-go/exporter/metric |
| github.com/GoogleCloudPlatform/opentelemetry-operations-go/internal/resourcemapping | v0.53.0 | src/go.mod | v0.62.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/GoogleCloudPlatform/opentelemetry-operations-go/internal/resourcemapping |
| github.com/gsterjov/go-libsecret | v0.0.0-20161001094733-a6f4afe4910c | src/go.mod | v0.0.0-20161001094733-a6f4afe4910c | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/gsterjov/go-libsecret |
| github.com/hashicorp/go-cleanhttp | v0.5.2 | src/go.mod | v0.5.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/hashicorp/go-cleanhttp |
| github.com/jmespath/go-jmespath | v0.4.0 | src/go.mod | v0.4.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/jmespath/go-jmespath |
| github.com/json-iterator/go | v1.1.12 | src/go.mod | v1.1.12 | CURRENT | Latest version source: https://pkg.go.dev/github.com/json-iterator/go |
| github.com/klauspost/asmfmt | v1.3.2 | src/go.mod | v1.3.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/klauspost/asmfmt |
| github.com/klauspost/compress | v1.18.0 | src/go.mod | v1.20.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/klauspost/compress |
| github.com/klauspost/cpuid/v2 | v2.2.11 | src/go.mod | v2.4.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/klauspost/cpuid/v2 |
| github.com/mattn/go-colorable | v0.1.15 | src/go.mod | v0.1.15 | CURRENT | Latest version source: https://pkg.go.dev/github.com/mattn/go-colorable |
| github.com/mattn/go-isatty | v0.0.22 | src/go.mod | v0.0.24 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/mattn/go-isatty |
| github.com/minio/asm2plan9s | v0.0.0-20200509001527-cdd76441f9d8 | src/go.mod | v0.0.0-20200509001527-cdd76441f9d8 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/minio/asm2plan9s |
| github.com/minio/c2goasm | v0.0.0-20190812172519-36a3d3bbc4f3 | src/go.mod | v0.0.0-20190812172519-36a3d3bbc4f3 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/minio/c2goasm |
| github.com/mitchellh/go-homedir | v1.1.0 | src/go.mod | v1.1.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/mitchellh/go-homedir |
| github.com/mitchellh/mapstructure | v1.5.0 | src/go.mod | v1.5.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/mitchellh/mapstructure |
| github.com/modern-go/concurrent | v0.0.0-20180306012644-bacd9c7ef1dd | src/go.mod | v0.0.0-20180306012644-bacd9c7ef1dd | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/modern-go/concurrent |
| github.com/modern-go/reflect2 | v1.0.2 | src/go.mod | v1.0.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/modern-go/reflect2 |
| github.com/mtibben/percent | v0.2.1 | src/go.mod | v0.2.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/mtibben/percent |
| github.com/munnerz/goautoneg | v0.0.0-20191010083416-a7dc8b61c822 | src/go.mod | v0.0.0-20191010083416-a7dc8b61c822 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/munnerz/goautoneg |
| github.com/peterhellberg/link | v1.2.0 | src/go.mod | v1.2.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/peterhellberg/link |
| github.com/pierrec/lz4/v4 | v4.1.22 | src/go.mod | v4.1.30 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/pierrec/lz4/v4 |
| github.com/pkg/browser | v0.0.0-20210911075715-681adbf594b8 | src/go.mod | v0.0.0-20240102092130-5ac0b6a4141c | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/pkg/browser |
| github.com/pkg/errors | v0.9.1 | src/go.mod | v0.9.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/pkg/errors |
| github.com/planetscale/vtprotobuf | v0.6.1-0.20240319094008-0393e58bdf10 | src/go.mod | v0.6.0 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/planetscale/vtprotobuf |
| github.com/pmezard/go-difflib | v1.0.1-0.20181226105442-5d4384ee4fb2 | src/go.mod | v1.0.0 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/pmezard/go-difflib |
| github.com/prometheus/client_golang | v1.22.0 | src/go.mod | v1.24.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/client_golang |
| github.com/prometheus/client_model | v0.6.2 | src/go.mod | v0.6.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/client_model |
| github.com/prometheus/common | v0.63.0 | src/go.mod | v0.71.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/common |
| github.com/prometheus/procfs | v0.16.1 | src/go.mod | v0.22.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/procfs |
| github.com/robfig/cron/v3 | v3.0.1 | src/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/robfig/cron/v3 |
| github.com/rs/zerolog | v1.34.0 | src/go.mod | v1.35.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/rs/zerolog |
| github.com/sirupsen/logrus | v1.9.3 | src/go.mod | v1.10.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/sirupsen/logrus |
| github.com/snowflakedb/gosnowflake | v1.19.1 | src/go.mod | v1.19.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/snowflakedb/gosnowflake |
| github.com/spiffe/go-spiffe/v2 | v2.6.0 | src/go.mod | v2.8.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/spiffe/go-spiffe/v2 |
| github.com/stretchr/testify | v1.11.1 | src/go.mod | v1.12.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/stretchr/testify |
| github.com/x448/float16 | v0.8.4 | src/go.mod | v0.8.4 | CURRENT | Latest version source: https://pkg.go.dev/github.com/x448/float16 |
| github.com/zeebo/xxh3 | v1.0.2 | src/go.mod | v1.1.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/zeebo/xxh3 |
| go.opentelemetry.io/auto/sdk | v1.2.1 | src/go.mod | v1.2.1 | CURRENT | Latest version source: https://pkg.go.dev/go.opentelemetry.io/auto/sdk |
| go.opentelemetry.io/contrib/detectors/gcp | v1.42.0 | src/go.mod | v1.46.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.opentelemetry.io/contrib/detectors/gcp |
| go.opentelemetry.io/contrib/instrumentation/google.golang.org/grpc/otelgrpc | v0.67.0 | src/go.mod | v0.71.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.opentelemetry.io/contrib/instrumentation/google.golang.org/grpc/otelgrpc |
| go.opentelemetry.io/contrib/instrumentation/net/http/otelhttp | v0.67.0 | src/go.mod | v0.71.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.opentelemetry.io/contrib/instrumentation/net/http/otelhttp |
| go.opentelemetry.io/otel | v1.44.0 | src/go.mod | v1.46.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.opentelemetry.io/otel |
| go.opentelemetry.io/otel/metric | v1.44.0 | src/go.mod | v1.46.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.opentelemetry.io/otel/metric |
| go.opentelemetry.io/otel/sdk | v1.44.0 | src/go.mod | v1.46.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.opentelemetry.io/otel/sdk |
| go.opentelemetry.io/otel/sdk/metric | v1.44.0 | src/go.mod | v1.46.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.opentelemetry.io/otel/sdk/metric |
| go.opentelemetry.io/otel/trace | v1.44.0 | src/go.mod | v1.46.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.opentelemetry.io/otel/trace |
| go.uber.org/atomic | v1.9.0 | src/go.mod | v1.12.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.uber.org/atomic |
| go.yaml.in/yaml/v2 | v2.4.4 | src/go.mod | v2.4.4 | CURRENT | Latest version source: https://pkg.go.dev/go.yaml.in/yaml/v2 |
| go.yaml.in/yaml/v3 | v3.0.4 | src/go.mod | v3.0.5 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.yaml.in/yaml/v3 |
| golang.org/x/crypto | v0.51.0 | src/go.mod | v0.57.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/crypto |
| golang.org/x/exp | v0.0.0-20250408133849-7e4ce0ab07d0 | src/go.mod | v0.0.0-20260908205506-85c1c2202aba | UNKNOWN | Latest version source: https://pkg.go.dev/golang.org/x/exp |
| golang.org/x/mod | v0.35.0 | src/go.mod | v0.41.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/mod |
| golang.org/x/net | v0.55.0 | src/go.mod | v0.59.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/net |
| golang.org/x/oauth2 | v0.36.0 | src/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/oauth2 |
| golang.org/x/sync | v0.20.0 | src/go.mod | v0.23.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/sync |
| golang.org/x/sys | v0.45.0 | src/go.mod | v0.48.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/sys |
| golang.org/x/telemetry | v0.0.0-20260409153401-be6f6cb8b1fa | src/go.mod | v0.0.0-20260910141331-15ceca2b0a1f | UNKNOWN | Latest version source: https://pkg.go.dev/golang.org/x/telemetry |
| golang.org/x/term | v0.43.0 | src/go.mod | v0.46.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/term |
| golang.org/x/text | v0.37.0 | src/go.mod | v0.42.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/text |
| golang.org/x/time | v0.15.0 | src/go.mod | v0.16.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/time |
| golang.org/x/tools | v0.44.0 | src/go.mod | v0.50.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/tools |
| golang.org/x/xerrors | v0.0.0-20240903120638-7835f813f4da | src/go.mod | v0.0.0-20240903120638-7835f813f4da | UNKNOWN | Latest version source: https://pkg.go.dev/golang.org/x/xerrors |
| google.golang.org/api | v0.279.0 | src/go.mod | v0.298.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/google.golang.org/api |
| google.golang.org/genproto | v0.0.0-20260610212136-7ab31c22f7ad | src/go.mod | v0.0.0-20260918162117-cecb64721679 | UNKNOWN | Latest version source: https://pkg.go.dev/google.golang.org/genproto |
| google.golang.org/genproto/googleapis/api | v0.0.0-20260610212136-7ab31c22f7ad | src/go.mod | v0.0.0-20260918162117-cecb64721679 | UNKNOWN | Latest version source: https://pkg.go.dev/google.golang.org/genproto/googleapis/api |
| google.golang.org/genproto/googleapis/rpc | v0.0.0-20260610212136-7ab31c22f7ad | src/go.mod | v0.0.0-20260918162117-cecb64721679 | UNKNOWN | Latest version source: https://pkg.go.dev/google.golang.org/genproto/googleapis/rpc |
| google.golang.org/grpc | v1.81.1 | src/go.mod | v1.84.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/google.golang.org/grpc |
| google.golang.org/protobuf | v1.36.11 | src/go.mod | v1.36.12 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/google.golang.org/protobuf |
| gopkg.in/evanphx/json-patch.v4 | v4.12.0 | src/go.mod | v4.13.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/gopkg.in/evanphx/json-patch.v4 |
| gopkg.in/inf.v0 | v0.9.1 | src/go.mod | v0.9.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/inf.v0 |
| gopkg.in/ini.v1 | v1.67.3 | src/go.mod | v1.67.3 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/ini.v1 |
| gopkg.in/yaml.v2 | v2.4.0 | src/go.mod | v2.4.0 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v2 |
| gopkg.in/yaml.v3 | v3.0.1 | src/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v3 |
| k8s.io/api | v0.32.13 | src/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/k8s.io/api |
| k8s.io/apimachinery | v0.32.13 | src/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/k8s.io/apimachinery |
| k8s.io/client-go | v0.32.13 | src/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/k8s.io/client-go |
| k8s.io/klog/v2 | v2.140.0 | src/go.mod | v2.140.0 | CURRENT | Latest version source: https://pkg.go.dev/k8s.io/klog/v2 |
| k8s.io/kube-openapi | v0.0.0-20250318190949-c8a335a9a2ff | src/go.mod | v0.0.0-20260911184034-7970a1e230da | UNKNOWN | Latest version source: https://pkg.go.dev/k8s.io/kube-openapi |
| k8s.io/utils | v0.0.0-20260507154919-ff6756f316d2 | src/go.mod | v0.0.0-20260707023825-cf1189d6abe3 | UNKNOWN | Latest version source: https://pkg.go.dev/k8s.io/utils |
| sigs.k8s.io/json | v0.0.0-20250730193827-2d320260d730 | src/go.mod | v0.0.0-20260909141634-11ed52e25bc5 | UNKNOWN | Latest version source: https://pkg.go.dev/sigs.k8s.io/json |
| sigs.k8s.io/randfill | v1.0.0 | src/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/sigs.k8s.io/randfill |
| sigs.k8s.io/structured-merge-diff/v4 | v4.6.0 | src/go.mod | v4.7.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/sigs.k8s.io/structured-merge-diff/v4 |
| sigs.k8s.io/yaml | v1.6.0 | src/go.mod | v1.6.0 | CURRENT | Latest version source: https://pkg.go.dev/sigs.k8s.io/yaml |

## 8. Tests and Coverage

- **Testing frameworks:** Testify
- **Test files detected:** 6
- **Coverage status:** Actual coverage result not found
- **Coverage percentage:** Not available
- **Coverage source:** Not available

## 9. Production Internal APIs

_Test/mock/example routes are excluded._

| Method | Endpoint | Handler | Component | Source File |
| --- | --- | --- | --- | --- |
| ROUTE | /residents | Not available | main | src/web/public/main.go |
| ROUTE | /ips | Not available | main | src/web/public/main.go |
| ROUTE | /ips/{category} | Not available | main | src/web/public/main.go |
| ROUTE | /accesses | Not available | main | src/web/private/main.go |
| ROUTE | /buckets | Not available | main | src/web/private/main.go |
| ROUTE | /bucket-rules | Not available | main | src/web/private/main.go |
| ROUTE | /cb-clusters | Not available | main | src/web/private/main.go |
| ROUTE | /certs | Not available | main | src/web/private/main.go |
| ROUTE | /cert-owners | Not available | main | src/web/private/main.go |
| ROUTE | /cert-summaries | Not available | main | src/web/private/main.go |
| ROUTE | /dynamo-dbs | Not available | main | src/web/private/main.go |
| ROUTE | /elasticaches | Not available | main | src/web/private/main.go |
| ROUTE | /instances | Not available | main | src/web/private/main.go |
| ROUTE | /instance-summaries | Not available | main | src/web/private/main.go |
| ROUTE | /ip-addresses | Not available | main | src/web/private/main.go |
| ROUTE | /k8s-clusters | Not available | main | src/web/private/main.go |
| ROUTE | /owners | Not available | main | src/web/private/main.go |
| ROUTE | /rds-instances | Not available | main | src/web/private/main.go |
| ROUTE | /support-plans | Not available | main | src/web/private/main.go |
| ROUTE | /users | Not available | main | src/web/private/main.go |
| ROUTE | /user-keys | Not available | main | src/web/private/main.go |
| ROUTE | /user-owners | Not available | main | src/web/private/main.go |
| ROUTE | /user-teams | Not available | main | src/web/private/main.go |
| ROUTE | /iam-summaries | Not available | main | src/web/private/main.go |
| ROUTE | /k8s-summaries | Not available | main | src/web/private/main.go |
| ROUTE | /volumes | Not available | main | src/web/private/main.go |
| ROUTE | /workloads | Not available | main | src/web/private/main.go |
| ROUTE | /healthz | Not available | main | src/web/private/main.go |

## 10. Production External API and Integration Calls

_Test/mock/example calls are excluded._

| Caller | Technology | Target | Method | Source File | Evidence |
| --- | --- | --- | --- | --- | --- |
| main | Go net/http | url | GET | src/cloud/lumen/main.go | http.NewRequest call |
| main | Go net/http | url | GET | src/cloud/comcast/main.go | http.NewRequest call |
| main | Go net/http | jiraURL | POST | src/utils/jira/main.go | http.NewRequest call |
| main | Go net/http | jiraSearchURL+"?jql="+jql | GET | src/utils/jira/main.go | http.NewRequest call |

## 11. Main Use Cases

No high-level use cases were returned by the local LLM.

## 12. Analysis Limitations

- Local LLM skipped; deterministic architecture and detailed static code flow are still reported.
