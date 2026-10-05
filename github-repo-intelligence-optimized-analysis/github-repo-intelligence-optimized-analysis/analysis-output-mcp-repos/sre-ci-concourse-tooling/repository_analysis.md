# Repository Intelligent Analysis Report

## 1. Repository Summary

- **Repository:** sre-ci-concourse-tooling
- **Source:** https://github.com/NBCUDTC/sre-ci-concourse-tooling.git
- **Source Type:** GitHub
- **Repository Type:** Application / Service / Library Repository
- **Files Analyzed:** 621
- **Local LLM Status:** Skipped by command line

### What the Application / Repository Does

Some directories have a tests folder. If it exists, go to that folder and run docker-compose up --build to build and run the docker image. The tests do not test all functionality of the docker images. They only serve as a small check that the docker image is built-able and can perform the most basic of tasks. You can run the /linting/do-linting.sh script (taking the base directory to lint as its only parameter) to check your code for issues that will potentially block pull request checks. The script will automatically use the .yamllint and .tflint.hcl config files used in PR checks, which are found in the /linting directory. Note that jsonlint may install as jsonlint depending on the method used, but the expected executable is jsonlint-php. If you have jsonlint on your system, symlink it to jsonlint-php to run this script. Note that you cannot symlink the do-linting.sh script because the check for config files will fail. However, it may be useful to add an executable script on your path that runs that script from its native directory.

### Repository Summary

Some directories have a tests folder. If it exists, go to that folder and run docker-compose up --build to build and run the docker image. The tests do not test all functionality of the docker images. They only serve as a small check that the docker image is built-able and can perform the most basic of tasks. You can run the /linting/do-linting.sh script (taking the base directory to lint as its only parameter) to check your code for issues that will potentially block pull request checks. The script will automatically use the .yamllint and .tflint.hcl config files used in PR checks, which are found in the /linting directory. Note that jsonlint may install as jsonlint depending on the method used, but the expected executable is jsonlint-php. If you have jsonlint on your system, symlink it to jsonlint-php to run this script. Note that you cannot symlink the do-linting.sh script because the check for config files will fail. However, it may be useful to add an executable script on your path that runs that script from its native directory.

## 2. Technology Stack

- **Languages:** Shell, Terraform, Go, JavaScript, Python
- **Frameworks:** Not detected
- **Runtime:** Go 1.19, Go 1.20, Go 1.23, Go 1.25.0, Go 1.25.11
- **Databases:** Not detected
- **Cloud Platforms:** Not detected
- **Containers:** Docker, Docker Compose
- **Kubernetes Helm Terraform:** Helm, Terraform
- **Ci Cd:** GitHub Actions
- **Testing Tools:** Mocha, Testify
- **Monitoring Observability:** Not detected
- **Important Core Libraries:** github.com/aws/aws-sdk-go, github.com/castai/promwrite, github.com/cespare/xxhash/v2, github.com/davecgh/go-spew, github.com/emicklei/go-restful/v3, github.com/fsnotify/fsnotify, github.com/fxamacker/cbor/v2, github.com/go-logr/logr, github.com/go-openapi/jsonpointer, github.com/go-openapi/jsonreference, github.com/go-openapi/swag, github.com/gogo/protobuf, github.com/golang/protobuf, github.com/golang/snappy, github.com/google/gnostic-models, github.com/google/go-cmp, github.com/google/go-github/v61, github.com/google/go-querystring, github.com/google/gofuzz, github.com/google/uuid, github.com/gorilla/websocket, github.com/grafana/regexp, github.com/hashicorp/hcl, github.com/jmespath/go-jmespath, github.com/josharian/intern, github.com/json-iterator/go, github.com/kr/pretty, github.com/magiconair/properties, github.com/mailru/easyjson, github.com/maxbrunsfeld/counterfeiter/v6, github.com/mitchellh/mapstructure, github.com/moby/spdystream, github.com/modern-go/concurrent, github.com/modern-go/reflect2, github.com/mongodb-forks/digest, github.com/munnerz/goautoneg, github.com/mxk/go-flowrate, github.com/pelletier/go-toml/v2, github.com/pkg/errors, github.com/pmezard/go-difflib, github.com/prometheus/client-model, github.com/prometheus/common, github.com/prometheus/prometheus, github.com/shurcool/githubv4, github.com/shurcool/graphql, github.com/spf13/afero, github.com/spf13/cast, github.com/spf13/jwalterweatherman, github.com/spf13/pflag, github.com/stretchr/testify, github.com/subosito/gotenv, github.com/x448/float16, go.mongodb.org/atlas-sdk/v20240805004, golang.org/x/mod, golang.org/x/net, golang.org/x/oauth2, golang.org/x/sys, golang.org/x/term, golang.org/x/text, golang.org/x/time, golang.org/x/tools, google.golang.org/protobuf, gopkg.in/evanphx/json-patch.v4, gopkg.in/inf.v0, gopkg.in/ini.v1, gopkg.in/yaml.v2, gopkg.in/yaml.v3, k8s.io/api, k8s.io/apimachinery, k8s.io/client-go, k8s.io/klog/v2, k8s.io/kube-openapi, k8s.io/utils, sigs.k8s.io/json, sigs.k8s.io/structured-merge-diff/v4, sigs.k8s.io/yaml

## 3. Repository Scan and Engineering Artifacts

- **Important files:** .github/workflows/build-artillery.yaml, .github/workflows/build-atlas.yaml, .github/workflows/build-aws-cli-runner.yaml, .github/workflows/build-bash-runner.yaml, .github/workflows/build-check-pr-branch-name.yaml, .github/workflows/build-check-pr-changes.yaml, .github/workflows/build-deploy-github-repos.yaml, .github/workflows/build-executor.yaml, .github/workflows/build-fetch-pr-titles.yaml, .github/workflows/build-flyway-mongo.yaml, .github/workflows/build-flyway.yaml, .github/workflows/build-gatling-simulation.yaml, .github/workflows/build-generate-pipeline.yaml, .github/workflows/build-github-governance.yaml, .github/workflows/build-github-pr-resource.yaml, .github/workflows/build-golang-unit-tests.yaml, .github/workflows/build-grafana-unit-tests.yaml, .github/workflows/build-helm-package.yaml, .github/workflows/build-linting.yaml, .github/workflows/build-manual-approval.yaml, .github/workflows/build-nodejs-tests.yaml, .github/workflows/build-notify-delivery-workflows.yaml, .github/workflows/build-packer.yaml, .github/workflows/build-predator.yaml, .github/workflows/build-prom-unit-tests.yaml, .github/workflows/build-python-runner.yaml, .github/workflows/build-snyk.yaml, .github/workflows/build-terraform-1-1-9.yaml, .github/workflows/build-terraform-1-11-4.yaml, .github/workflows/build-terraform-1-4-5.yaml, .github/workflows/build-terraform-1-5-3.yaml, .github/workflows/build-terraform.yaml, .github/workflows/build-tf-module-to-gcs.yaml, .github/workflows/build-tf-module-to-s3.yaml, .github/workflows/build-tf-plan-output-to-pr.yaml, .github/workflows/build-validate-prom-config.yaml, .github/workflows/build-validate-prom-targets.yaml, .github/workflows/build-ytt-and-fly.yaml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/pr-reviews.yaml, .github/workflows/pr-title-validation.yaml, .github/workflows/set-self.yaml, .github/workflows/setup-repository.yaml, README.md

- **Configuration:** flyway/test/config/docker-flyway.config, ytt-and-fly/templates/config/jobs.lib.yml, ytt-and-fly/templates/config/main.yml, ytt-and-fly/templates/config/resource_types.lib.yml, ytt-and-fly/templates/config/resources.lib.yml, ytt-and-fly/templates/config/steps.lib.yml
- **Docker:** artillery/Dockerfile, artillery/tests/docker-compose.yaml, atlas/Dockerfile, atlas/docker-compose.yml, aws-cli-runner/Dockerfile, aws-cli-runner/tests/docker-compose.yml, bash-runner/Dockerfile, changie-tool/test/docker-compose.yaml, check-pr-branch-name/Dockerfile, check-pr-branch-name/test/docker-compose.yml, check-pr-changes/Dockerfile, databricks/Dockerfile, databricks/test/docker-compose.yml, deploy-github-repos/Dockerfile, deploy-github-repos/test/docker-compose.yml, executor-kubectl/docker-compose.yml, executor/Dockerfile, executor/docker-compose.yml, fah-gradle-publish/tests/docker-compose.yaml, fetch-pr-titles/Dockerfile, flyway-mongo/Dockerfile, flyway-mongo/test/docker-compose.yml, flyway/Dockerfile, flyway/test/Dockerfile, flyway/test/docker-compose.yml, gatling-simulation/Dockerfile, gatling-simulation/tests/docker-compose.yaml, generate-pipeline/Dockerfile, generate-pipeline/test/docker-compose.yml, github-governance/Dockerfile, github-governance/tests/docker-compose.yaml, github-pr-resource/Dockerfile, golang-unit-tests/Dockerfile, golang-unit-tests/test/docker-compose.yml, grafana-unit-tests/Dockerfile, helm-package/Dockerfile, helm-package/tests/docker-compose.yaml, lambda-zip-s3/Dockerfile, lambda-zip-s3/tests/docker-compose.yaml, linting/Dockerfile, linting/tests/docker-compose.yaml, manual-approval/Dockerfile, manual-approval/tests/docker-compose.yaml, nodejs-tests/Dockerfile, nodejs-tests/tests/docker-compose.yaml, notify-delivery-workflows/Dockerfile, packer/Dockerfile, packer/tests/docker-compose.yml, predator/Dockerfile, prom-unit-tests/Dockerfile, prom-unit-tests/tests/docker-compose.yaml, python-runner/Dockerfile, python-runner/tests/docker-compose.yml, snyk/Dockerfile, terraform-1-1-9/Dockerfile, terraform-1-1-9/tests/docker-compose.yml, terraform-1-11-4/Dockerfile, terraform-1-11-4/tests/docker-compose.yml, terraform-1-4-5/Dockerfile, terraform-1-4-5/tests/docker-compose.yml, terraform-1-5-3/Dockerfile, terraform-1-5-3/tests/docker-compose.yml, terraform/Dockerfile, terraform/tests/docker-compose.yml, terransible-1-1-9/Dockerfile, terransible/Dockerfile, terratest/Dockerfile, terratest/tests/docker-compose.yml, tf-module-to-gcs/Dockerfile, tf-module-to-gcs/tests/docker-compose.yaml, tf-module-to-s3/Dockerfile, tf-module-to-s3/tests/docker-compose.yaml, tf-plan-output-to-pr/Dockerfile, tf-plan-output-to-pr/tests/docker-compose.yaml, validate-prom-config/Dockerfile, validate-prom-config/tests/docker-compose.yaml, validate-prom-targets/Dockerfile, validate-prom-targets/tests/docker-compose.yaml, ytt-and-fly/Dockerfile
- **Kubernetes Helm:** helm-package/tests/chart/Chart.yaml, linting/tests/chart-with-library/Chart.yaml, linting/tests/chart/Chart.yaml, linting/tests/chart/charts/subchart/.helmignore, linting/tests/chart/charts/subchart/Chart.yaml, linting/tests/chart/charts/subchart/templates/NOTES.txt, linting/tests/chart/charts/subchart/templates/_helpers.tpl, linting/tests/chart/charts/subchart/templates/deployment.yaml, linting/tests/chart/charts/subchart/templates/hpa.yaml, linting/tests/chart/charts/subchart/templates/ingress.yaml, linting/tests/chart/charts/subchart/templates/service.yaml, linting/tests/chart/charts/subchart/templates/serviceaccount.yaml, linting/tests/chart/charts/subchart/templates/tests/test-connection.yaml, linting/tests/chart/charts/subchart/values.yaml, linting/tests/library/Chart.yaml
- **Terraform:** deploy-github-repos/test/test.tf, lambda-zip-s3/tests/git-repo/src/main.tf, linting/tests/terraform/main.tf, linting/tests/terraform/outputs.tf, linting/tests/terraform/variables.tf, terraform-1-1-9/tests/atlas-cluster.tf, terraform-1-1-9/tests/aws-config.tf, terraform-1-1-9/tests/gke-config.tf, terraform-1-1-9/tests/main.tf, terraform-1-1-9/tests/modules/custom-role/main.tf, terraform-1-1-9/tests/modules/custom-role/variables.tf, terraform-1-1-9/tests/modules/s3-buckets/s3-buckets.tf, terraform-1-1-9/tests/modules/s3-buckets/variables.tf, terraform-1-1-9/tests/project.tf, terraform-1-11-4/tests/atlas-cluster.tf, terraform-1-11-4/tests/aws-config.tf, terraform-1-11-4/tests/gke-config.tf, terraform-1-11-4/tests/main.tf, terraform-1-11-4/tests/modules/custom-role/main.tf, terraform-1-11-4/tests/modules/custom-role/variables.tf, terraform-1-11-4/tests/modules/s3-buckets/s3-buckets.tf, terraform-1-11-4/tests/modules/s3-buckets/variables.tf, terraform-1-11-4/tests/project.tf, terraform-1-4-5/tests/atlas-cluster.tf, terraform-1-4-5/tests/aws-config.tf, terraform-1-4-5/tests/gke-config.tf, terraform-1-4-5/tests/main.tf, terraform-1-4-5/tests/modules/custom-role/main.tf, terraform-1-4-5/tests/modules/custom-role/variables.tf, terraform-1-4-5/tests/modules/s3-buckets/s3-buckets.tf, terraform-1-4-5/tests/modules/s3-buckets/variables.tf, terraform-1-4-5/tests/project.tf, terraform-1-5-3/tests/atlas-cluster.tf, terraform-1-5-3/tests/aws-config.tf, terraform-1-5-3/tests/gke-config.tf, terraform-1-5-3/tests/main.tf, terraform-1-5-3/tests/modules/custom-role/main.tf, terraform-1-5-3/tests/modules/custom-role/variables.tf, terraform-1-5-3/tests/modules/s3-buckets/s3-buckets.tf, terraform-1-5-3/tests/modules/s3-buckets/variables.tf, terraform-1-5-3/tests/project.tf, terraform/tests/atlas-cluster.tf, terraform/tests/aws-config.tf, terraform/tests/gke-config.tf, terraform/tests/main.tf, terraform/tests/modules/custom-role/main.tf, terraform/tests/modules/custom-role/variables.tf, terraform/tests/modules/s3-buckets/s3-buckets.tf, terraform/tests/modules/s3-buckets/variables.tf, terraform/tests/project.tf, terratest/tests/main.tf, tf-module-to-gcs/tests/git-repo/src/main.tf, tf-module-to-s3/tests/git-repo/src/main.tf
- **Ci Cd:** .github/workflows/build-artillery.yaml, .github/workflows/build-atlas.yaml, .github/workflows/build-aws-cli-runner.yaml, .github/workflows/build-bash-runner.yaml, .github/workflows/build-check-pr-branch-name.yaml, .github/workflows/build-check-pr-changes.yaml, .github/workflows/build-deploy-github-repos.yaml, .github/workflows/build-executor.yaml, .github/workflows/build-fetch-pr-titles.yaml, .github/workflows/build-flyway-mongo.yaml, .github/workflows/build-flyway.yaml, .github/workflows/build-gatling-simulation.yaml, .github/workflows/build-generate-pipeline.yaml, .github/workflows/build-github-governance.yaml, .github/workflows/build-github-pr-resource.yaml, .github/workflows/build-golang-unit-tests.yaml, .github/workflows/build-grafana-unit-tests.yaml, .github/workflows/build-helm-package.yaml, .github/workflows/build-linting.yaml, .github/workflows/build-manual-approval.yaml, .github/workflows/build-nodejs-tests.yaml, .github/workflows/build-notify-delivery-workflows.yaml, .github/workflows/build-packer.yaml, .github/workflows/build-predator.yaml, .github/workflows/build-prom-unit-tests.yaml, .github/workflows/build-python-runner.yaml, .github/workflows/build-snyk.yaml, .github/workflows/build-terraform-1-1-9.yaml, .github/workflows/build-terraform-1-11-4.yaml, .github/workflows/build-terraform-1-4-5.yaml, .github/workflows/build-terraform-1-5-3.yaml, .github/workflows/build-terraform.yaml, .github/workflows/build-tf-module-to-gcs.yaml, .github/workflows/build-tf-module-to-s3.yaml, .github/workflows/build-tf-plan-output-to-pr.yaml, .github/workflows/build-validate-prom-config.yaml, .github/workflows/build-validate-prom-targets.yaml, .github/workflows/build-ytt-and-fly.yaml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/pr-reviews.yaml, .github/workflows/pr-title-validation.yaml, .github/workflows/set-self.yaml, .github/workflows/setup-repository.yaml
- **Api Specs:** Not detected
- **Documentation:** README.md, artillery/README.md, changie-tool/test/README.md, gatling-simulation/tests/README.md, github-governance/README.md, github-pr-resource/README.md, misc-files/README.md, prom-unit-tests/prom-unit-test-acceptance/README.md, terraform-1-1-9/tests/README.md, terraform-1-11-4/tests/README.md, terraform-1-4-5/tests/README.md, terraform-1-5-3/tests/README.md, terraform/tests/README.md

## 4. Main Components and Code Structure

### ytt-and-fly
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 128 analyzed core files under ytt-and-fly/

### .github
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 46 analyzed core files under .github/

### github-pr-resource
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 22 analyzed core files under github-pr-resource/

### terraform-1-1-9
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 10 analyzed core files under terraform-1-1-9/

### terraform-1-4-5
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 10 analyzed core files under terraform-1-4-5/

### terraform-1-5-3
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 10 analyzed core files under terraform-1-5-3/

### artillery
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 10 analyzed core files under artillery/

### terraform
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 9 analyzed core files under terraform/

### golang-unit-tests
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 9 analyzed core files under golang-unit-tests/

### prom-unit-tests
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 9 analyzed core files under prom-unit-tests/

### linting
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 8 analyzed core files under linting/

### terraform-1-11-4
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 8 analyzed core files under terraform-1-11-4/

### validate-prom-config
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 7 analyzed core files under validate-prom-config/

### snyk
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 7 analyzed core files under snyk/

### grafana-unit-tests
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 7 analyzed core files under grafana-unit-tests/

## 5. Code Architecture

- **Architecture Style:** Modular repository architecture
- **Architecture Explanation:** The repository follows a modular repository architecture. Static analysis identified 15 major structural component areas, 11 executable/package entry points, and 0 repository-local dependency relationships. The architecture below is generated from source layout, imports, symbols, package metadata and executable entry points; the local LLM is used only to explain these facts in repository-specific language.

### Layers / Modules

| Layer / Module | Description | Evidence |
| --- | --- | --- |
| ytt-and-fly | Top-level source/component area; semantic responsibility refined by local LLM | 128 analyzed core files under ytt-and-fly/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 46 analyzed core files under .github/ |
| github-pr-resource | Top-level source/component area; semantic responsibility refined by local LLM | 22 analyzed core files under github-pr-resource/ |
| terraform-1-1-9 | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under terraform-1-1-9/ |
| terraform-1-4-5 | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under terraform-1-4-5/ |
| terraform-1-5-3 | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under terraform-1-5-3/ |
| artillery | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under artillery/ |
| terraform | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under terraform/ |
| golang-unit-tests | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under golang-unit-tests/ |
| prom-unit-tests | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under prom-unit-tests/ |
| linting | Top-level source/component area; semantic responsibility refined by local LLM | 8 analyzed core files under linting/ |
| terraform-1-11-4 | Top-level source/component area; semantic responsibility refined by local LLM | 8 analyzed core files under terraform-1-11-4/ |
| validate-prom-config | Top-level source/component area; semantic responsibility refined by local LLM | 7 analyzed core files under validate-prom-config/ |
| snyk | Top-level source/component area; semantic responsibility refined by local LLM | 7 analyzed core files under snyk/ |
| grafana-unit-tests | Top-level source/component area; semantic responsibility refined by local LLM | 7 analyzed core files under grafana-unit-tests/ |

### Entry Points

| Type | Symbol / Command | Source File |
| --- | --- | --- |
| Go executable entry point | atlas:main | atlas/main.go |
| Go executable entry point | artillery/src:main | artillery/src/main.go |
| Go executable entry point | prom-unit-tests/prom-unit-test-acceptance:main | prom-unit-tests/prom-unit-test-acceptance/main.go |
| Go executable entry point | validate-prom-targets/src:main | validate-prom-targets/src/main.go |
| Go executable entry point | grafana-unit-tests/grafana-unit-tests-coverage:main | grafana-unit-tests/grafana-unit-tests-coverage/main.go |
| Go executable entry point | tf-plan-output-to-pr/src:main | tf-plan-output-to-pr/src/main.go |
| Go executable entry point | snyk/app:main | snyk/app/main.go |
| Go executable entry point | github-pr-resource/cmd/out:main | github-pr-resource/cmd/out/main.go |
| Go executable entry point | github-pr-resource/cmd/in:main | github-pr-resource/cmd/in/main.go |
| Go executable entry point | github-pr-resource/cmd/check:main | github-pr-resource/cmd/check/main.go |
| Go executable entry point | validate-prom-config/src:main | validate-prom-config/src/main.go |

### Major Components

| Component | Responsibility | Evidence |
| --- | --- | --- |
| ytt-and-fly | Top-level source/component area; semantic responsibility refined by local LLM | 128 analyzed core files under ytt-and-fly/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 46 analyzed core files under .github/ |
| github-pr-resource | Top-level source/component area; semantic responsibility refined by local LLM | 22 analyzed core files under github-pr-resource/ |
| terraform-1-1-9 | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under terraform-1-1-9/ |
| terraform-1-4-5 | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under terraform-1-4-5/ |
| terraform-1-5-3 | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under terraform-1-5-3/ |
| artillery | Top-level source/component area; semantic responsibility refined by local LLM | 10 analyzed core files under artillery/ |
| terraform | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under terraform/ |
| golang-unit-tests | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under golang-unit-tests/ |
| prom-unit-tests | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under prom-unit-tests/ |
| linting | Top-level source/component area; semantic responsibility refined by local LLM | 8 analyzed core files under linting/ |
| terraform-1-11-4 | Top-level source/component area; semantic responsibility refined by local LLM | 8 analyzed core files under terraform-1-11-4/ |
| validate-prom-config | Top-level source/component area; semantic responsibility refined by local LLM | 7 analyzed core files under validate-prom-config/ |
| snyk | Top-level source/component area; semantic responsibility refined by local LLM | 7 analyzed core files under snyk/ |
| grafana-unit-tests | Top-level source/component area; semantic responsibility refined by local LLM | 7 analyzed core files under grafana-unit-tests/ |

### Component Relationships

_Not detected._

### Configuration Model

Repository contains explicit configuration artifacts: flyway/test/config/docker-flyway.config, ytt-and-fly/templates/config/jobs.lib.yml, ytt-and-fly/templates/config/main.yml, ytt-and-fly/templates/config/resource_types.lib.yml, ytt-and-fly/templates/config/resources.lib.yml, ytt-and-fly/templates/config/steps.lib.yml.

### Extension Points

No explicit extension points were statically identified.

### Deployment Model

Docker, Kubernetes/Helm, Terraform-managed infrastructure

### Architecture Data / Control Flow

1. Execution begins at the detected repository entry point(s): atlas/main.go, artillery/src/main.go, prom-unit-tests/prom-unit-test-acceptance/main.go, validate-prom-targets/src/main.go, grafana-unit-tests/grafana-unit-tests-coverage/main.go, tf-plan-output-to-pr/src/main.go, snyk/app/main.go, github-pr-resource/cmd/out/main.go.
2. Configuration artifacts influence component initialization and runtime behavior.
3. Core components process requests/commands/events through repository modules and return results to the caller or downstream integration.

## 6. Overall Code Flow

- **Code Flow Analysis Status:** Deterministic static code-flow fallback (--skip-llm)

This section explains the repository flow in simple execution order. It separates the main runtime from independent automation/tooling paths and only uses code/source evidence found in the repository.

### Flow Overview

The repository runtime starts from its executable entry point, loads configuration and infrastructure dependencies, registers production routes, and starts the service. Each request then follows the statically resolved handler -> use case/service -> repository -> DAL/client path where such a chain is proven. Persistence operations are shown only when directly detected in source. The service closes through its graceful shutdown path when one is present.

### Application Startup Flow

#### Step 1: Start the application

Execution starts in atlas/main.go at main. The startup function then delegates into the application bootstrap code shown below.

**Code / files involved:**
- `atlas/main.go:main`
- `os.Getenv`
- `context.Background`
- `ProjectsApi.GetProjectByName`
- `log.Printf`
- `ClustersApi.GetCluster`
- `getClient`
- `StartCluster`

**What happens next:** Control moves into application initialization.

**Evidence:** atlas/main.go

#### Step 2: Load runtime configuration

The application uses the detected configuration files during startup. Configuration values control later runtime initialization; values not proven from source are not guessed.

**Code / files involved:**
- `flyway/test/config/docker-flyway.config`
- `ytt-and-fly/templates/config/jobs.lib.yml`
- `ytt-and-fly/templates/config/main.yml`
- `ytt-and-fly/templates/config/resource_types.lib.yml`
- `ytt-and-fly/templates/config/resources.lib.yml`
- `ytt-and-fly/templates/config/steps.lib.yml`

**What happens next:** Validated runtime settings are available to the bootstrap code.

**Evidence:** flyway/test/config/docker-flyway.config, ytt-and-fly/templates/config/jobs.lib.yml, ytt-and-fly/templates/config/main.yml, ytt-and-fly/templates/config/resource_types.lib.yml, ytt-and-fly/templates/config/resources.lib.yml, ytt-and-fly/templates/config/steps.lib.yml

#### Step 3: Build application dependencies and start the server

The main bootstrap creates the runtime dependencies in code order. The detected calls include logging/metrics setup, database/client connection, repository/use-case/handler construction, HTTP server creation and service start where present.

**Code / files involved:**
- `snyk/app/main.go:main`
- `time.Now`
- `viper.AutomaticEnv`
- `viper.GetString`
- `endTime.Sub`
- `fmt.Println`
- `RetrieveTargetId`
- `GatherProjectIDs`
- `CreateIssueReport`

**What happens next:** The service is initialized and ready to receive runtime work.

**Evidence:** snyk/app/main.go

### Static Call / Module Paths

The paths below are the exact callable/import chains that static analysis could prove. They support the simplified flow above.

No complete callable chain was statically provable for this repository.

## 7. Dependencies and Compatibility

Dependencies are grouped by scope. Example/test/documentation dependencies do not contaminate the core technology stack.

### Core Dependencies

| Dependency | Current Version / Constraint | Source | Latest Version | Compatibility | Notes |
| --- | --- | --- | --- | --- | --- |
| github.com/aws/aws-sdk-go | v1.55.7 | artillery/src/go.mod | v1.55.8 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/aws/aws-sdk-go |
| github.com/castai/promwrite | v0.6.0 | artillery/src/go.mod | v0.6.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/castai/promwrite |
| github.com/cespare/xxhash/v2 | v2.3.0 | artillery/src/go.mod | v2.3.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/cespare/xxhash/v2 |
| github.com/davecgh/go-spew | v1.1.1 | github-pr-resource/go.mod | v1.1.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/davecgh/go-spew |
| github.com/davecgh/go-spew | v1.1.2-0.20180830191138-d8f796af33cc | artillery/src/go.mod | v1.1.1 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/davecgh/go-spew |
| github.com/emicklei/go-restful/v3 | v3.11.0 | artillery/src/go.mod | v3.13.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/emicklei/go-restful/v3 |
| github.com/fsnotify/fsnotify | v1.6.0 | snyk/app/go.mod | v1.10.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/fsnotify/fsnotify |
| github.com/fxamacker/cbor/v2 | v2.7.0 | artillery/src/go.mod | v2.9.4 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/fxamacker/cbor/v2 |
| github.com/go-logr/logr | v1.4.2 | artillery/src/go.mod | v1.4.4 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-logr/logr |
| github.com/go-openapi/jsonpointer | v0.21.0 | artillery/src/go.mod | v1.0.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/jsonpointer |
| github.com/go-openapi/jsonreference | v0.21.0 | artillery/src/go.mod | v1.0.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/jsonreference |
| github.com/go-openapi/swag | v0.23.0 | artillery/src/go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag |
| github.com/gogo/protobuf | v1.3.2 | artillery/src/go.mod | v1.3.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/gogo/protobuf |
| github.com/golang/protobuf | v1.5.4 | artillery/src/go.mod | v1.5.4 | CURRENT | Latest version source: https://pkg.go.dev/github.com/golang/protobuf |
| github.com/golang/snappy | v1.0.0 | artillery/src/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/golang/snappy |
| github.com/google/gnostic-models | v0.6.8 | artillery/src/go.mod | v0.7.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/google/gnostic-models |
| github.com/google/go-cmp | v0.7.0 | artillery/src/go.mod | v0.7.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/google/go-cmp |
| github.com/google/go-github/v61 | v61.0.0 | github-pr-resource/go.mod | v61.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/google/go-github/v61 |
| github.com/google/go-querystring | v1.1.0 | github-pr-resource/go.mod | v1.2.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/google/go-querystring |
| github.com/google/gofuzz | v1.2.0 | artillery/src/go.mod | v1.2.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/google/gofuzz |
| github.com/google/uuid | v1.6.0 | artillery/src/go.mod | v1.6.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/google/uuid |
| github.com/gorilla/websocket | v1.5.0 | artillery/src/go.mod | v1.5.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/gorilla/websocket |
| github.com/grafana/regexp | v0.0.0-20240518133315-a468a5bfb3bc | artillery/src/go.mod | v0.0.0-20250905093917-f7b3be9d1853 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/grafana/regexp |
| github.com/hashicorp/hcl | v1.0.0 | snyk/app/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/hashicorp/hcl |
| github.com/jmespath/go-jmespath | v0.4.0 | artillery/src/go.mod | v0.4.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/jmespath/go-jmespath |
| github.com/josharian/intern | v1.0.0 | artillery/src/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/josharian/intern |
| github.com/json-iterator/go | v1.1.12 | artillery/src/go.mod | v1.1.12 | CURRENT | Latest version source: https://pkg.go.dev/github.com/json-iterator/go |
| github.com/kr/pretty | v0.3.1 | github-pr-resource/go.mod | v0.3.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/kr/pretty |
| github.com/magiconair/properties | v1.8.7 | snyk/app/go.mod | v1.18.12 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/magiconair/properties |
| github.com/mailru/easyjson | v0.7.7 | artillery/src/go.mod | v0.9.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/mailru/easyjson |
| github.com/maxbrunsfeld/counterfeiter/v6 | v6.8.1 | github-pr-resource/go.mod | v6.13.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/maxbrunsfeld/counterfeiter/v6 |
| github.com/mitchellh/mapstructure | v1.5.0 | snyk/app/go.mod | v1.5.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/mitchellh/mapstructure |
| github.com/moby/spdystream | v0.5.1 | artillery/src/go.mod | v0.5.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/moby/spdystream |
| github.com/modern-go/concurrent | v0.0.0-20180306012644-bacd9c7ef1dd | artillery/src/go.mod | v0.0.0-20180306012644-bacd9c7ef1dd | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/modern-go/concurrent |
| github.com/modern-go/reflect2 | v1.0.2 | artillery/src/go.mod | v1.0.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/modern-go/reflect2 |
| github.com/mongodb-forks/digest | v1.1.0 | atlas/go.mod | v1.1.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/mongodb-forks/digest |
| github.com/munnerz/goautoneg | v0.0.0-20191010083416-a7dc8b61c822 | artillery/src/go.mod | v0.0.0-20191010083416-a7dc8b61c822 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/munnerz/goautoneg |
| github.com/mxk/go-flowrate | v0.0.0-20140419014527-cca7078d478f | artillery/src/go.mod | v0.0.0-20140419014527-cca7078d478f | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/mxk/go-flowrate |
| github.com/pelletier/go-toml/v2 | v2.0.8 | snyk/app/go.mod | v2.4.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/pelletier/go-toml/v2 |
| github.com/pkg/errors | v0.9.1 | artillery/src/go.mod | v0.9.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/pkg/errors |
| github.com/pmezard/go-difflib | v1.0.0 | github-pr-resource/go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/pmezard/go-difflib |
| github.com/prometheus/client_model | v0.6.2 | artillery/src/go.mod | v0.6.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/client_model |
| github.com/prometheus/common | v0.63.0 | artillery/src/go.mod | v0.71.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/common |
| github.com/prometheus/prometheus | v0.304.1 | artillery/src/go.mod | v0.314.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/prometheus |
| github.com/shurcooL/githubv4 | v0.0.0-20240727222349-48295856cce7 | github-pr-resource/go.mod | v0.0.0-20260209031235-2402fdf4a9ed | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/shurcooL/githubv4 |
| github.com/shurcooL/graphql | v0.0.0-20230722043721-ed46e5a46466 | github-pr-resource/go.mod | v0.0.0-20240915155400-7ee5256398cf | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/shurcooL/graphql |
| github.com/spf13/afero | v1.9.5 | snyk/app/go.mod | v1.15.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/spf13/afero |
| github.com/spf13/cast | v1.5.1 | snyk/app/go.mod | v1.10.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/spf13/cast |
| github.com/spf13/jwalterweatherman | v1.1.0 | snyk/app/go.mod | v1.1.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/spf13/jwalterweatherman |
| github.com/spf13/pflag | v1.0.5 | snyk/app/go.mod | v1.0.10 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/spf13/pflag |
| github.com/stretchr/testify | v1.10.0 | github-pr-resource/go.mod | v1.12.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/stretchr/testify |
| github.com/subosito/gotenv | v1.4.2 | snyk/app/go.mod | v1.6.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/subosito/gotenv |
| github.com/x448/float16 | v0.8.4 | artillery/src/go.mod | v0.8.4 | CURRENT | Latest version source: https://pkg.go.dev/github.com/x448/float16 |
| go.mongodb.org/atlas-sdk/v20240805004 | v20240805004.7.0 | atlas/go.mod | v20240805004.7.0 | CURRENT | Latest version source: https://pkg.go.dev/go.mongodb.org/atlas-sdk/v20240805004 |
| golang.org/x/mod | v0.14.0 | github-pr-resource/go.mod | v0.41.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/mod |
| golang.org/x/net | v0.54.0 | artillery/src/go.mod | v0.59.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/net |
| golang.org/x/oauth2 | v0.28.0 | github-pr-resource/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/oauth2 |
| golang.org/x/oauth2 | v0.29.0 | artillery/src/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/oauth2 |
| golang.org/x/sys | v0.44.0 | artillery/src/go.mod | v0.48.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/sys |
| golang.org/x/sys | v0.8.0 | snyk/app/go.mod | v0.48.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/sys |
| golang.org/x/term | v0.43.0 | artillery/src/go.mod | v0.46.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/term |
| golang.org/x/text | v0.14.0 | github-pr-resource/go.mod | v0.42.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/text |
| golang.org/x/text | v0.37.0 | artillery/src/go.mod | v0.42.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/text |
| golang.org/x/text | v0.9.0 | snyk/app/go.mod | v0.42.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/text |
| golang.org/x/time | v0.11.0 | artillery/src/go.mod | v0.16.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/time |
| golang.org/x/tools | v0.17.0 | github-pr-resource/go.mod | v0.50.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/tools |
| google.golang.org/protobuf | v1.36.6 | artillery/src/go.mod | v1.36.12 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/google.golang.org/protobuf |
| gopkg.in/evanphx/json-patch.v4 | v4.12.0 | artillery/src/go.mod | v4.13.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/gopkg.in/evanphx/json-patch.v4 |
| gopkg.in/inf.v0 | v0.9.1 | artillery/src/go.mod | v0.9.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/inf.v0 |
| gopkg.in/ini.v1 | v1.67.0 | snyk/app/go.mod | v1.67.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/gopkg.in/ini.v1 |
| gopkg.in/yaml.v2 | v2.4.0 | artillery/src/go.mod | v2.4.0 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v2 |
| gopkg.in/yaml.v3 | v3.0.1 | github-pr-resource/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v3 |
| gopkg.in/yaml.v3 | v3.0.1 | artillery/src/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v3 |
| gopkg.in/yaml.v3 | v3.0.1 | snyk/app/go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v3 |
| k8s.io/api | v0.32.3 | artillery/src/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/k8s.io/api |
| k8s.io/apimachinery | v0.32.3 | artillery/src/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/k8s.io/apimachinery |
| k8s.io/client-go | v0.32.3 | artillery/src/go.mod | v0.37.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/k8s.io/client-go |
| k8s.io/klog/v2 | v2.130.1 | artillery/src/go.mod | v2.140.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/k8s.io/klog/v2 |
| k8s.io/kube-openapi | v0.0.0-20241105132330-32ad38e42d3f | artillery/src/go.mod | v0.0.0-20260911184034-7970a1e230da | UNKNOWN | Latest version source: https://pkg.go.dev/k8s.io/kube-openapi |
| k8s.io/utils | v0.0.0-20241104100929-3ea5e8cea738 | artillery/src/go.mod | v0.0.0-20260707023825-cf1189d6abe3 | UNKNOWN | Latest version source: https://pkg.go.dev/k8s.io/utils |
| sigs.k8s.io/json | v0.0.0-20241010143419-9aa6b5e7a4b3 | artillery/src/go.mod | v0.0.0-20260909141634-11ed52e25bc5 | UNKNOWN | Latest version source: https://pkg.go.dev/sigs.k8s.io/json |
| sigs.k8s.io/structured-merge-diff/v4 | v4.4.2 | artillery/src/go.mod | v4.7.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/sigs.k8s.io/structured-merge-diff/v4 |
| sigs.k8s.io/yaml | v1.4.0 | artillery/src/go.mod | v1.6.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/sigs.k8s.io/yaml |

### Test Dependencies

| Dependency | Current Version / Constraint | Source | Latest Version | Compatibility | Notes |
| --- | --- | --- | --- | --- | --- |
| boto3 | Not available | python-runner/tests/requirements.txt | Not available | Not checked - non-core dependency | Not available |
| mocha | ^8.3.2 | nodejs-tests/tests/git-repo/src/package.json | Not available | Not checked - non-core dependency | Not available |

## 8. Tests and Coverage

- **Testing frameworks:** Mocha, Testify
- **Test files detected:** 172
- **Coverage status:** Actual coverage result not found
- **Coverage percentage:** Not available
- **Coverage source:** Not available

## 9. Production Internal APIs

_Test/mock/example routes are excluded._

_Not detected._

## 10. Production External API and Integration Calls

_Test/mock/example calls are excluded._

| Caller | Technology | Target | Method | Source File | Evidence |
| --- | --- | --- | --- | --- | --- |
| github | GitHub client library | GitHub API | SDK | github-pr-resource/github.go | GitHub client usage detected |
| main | Go net/http | URL | GET | snyk/app/main.go | http.NewRequest call |
| main | Go net/http | URL | POST | snyk/app/main.go | http.NewRequest call |

## 11. Main Use Cases

No high-level use cases were returned by the local LLM.

## 12. Analysis Limitations

- Local LLM skipped; deterministic architecture and detailed static code flow are still reported.
