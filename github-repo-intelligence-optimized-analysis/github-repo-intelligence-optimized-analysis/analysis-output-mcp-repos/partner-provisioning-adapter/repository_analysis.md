# Repository Intelligent Analysis Report

## 1. Repository Summary

- **Repository:** partner-provisioning-adapter
- **Source:** https://github.com/NBCUDTC/partner-provisioning-adapter.git
- **Source Type:** GitHub
- **Repository Type:** Application / Service / Library Repository
- **Files Analyzed:** 652
- **Local LLM Status:** Skipped by command line

### What the Application / Repository Does

To run PPA with its dependencies: [Optional: Add --build to rebuild the service and other images before running] To stop PPA and its dependencies: SonarQube is currently disabled while the project os being developed, if a scan is required, the code in the cdBuild.sh can be uncommented and run via a branch build in Jenkins. In order for our application to work with Java 21 we need to install the OpenJDK 21 on our machine and make it available After this we can configure in Intellij that our project uses java 21 by pointing to use /Library/Java/JavaVirtualMachines/jdk-21 folder as the source for the JDK. 1. Start the dynamodb-init Docker container. 2. Open the "Database" sidebar in IntelliJ and click the plus icon. 3. Select DynamoDB as the data source and fill in with the following details then connect: 5. The table(s) present in the Dockerised DynamoDB should now be visible in the Database sidebar. 6. There will be no items in the table unless you populate it somehow, either using a PPA endpoint, or manually interacting with the database.

### Repository Summary

To run PPA with its dependencies: [Optional: Add --build to rebuild the service and other images before running] To stop PPA and its dependencies: SonarQube is currently disabled while the project os being developed, if a scan is required, the code in the cdBuild.sh can be uncommented and run via a branch build in Jenkins. In order for our application to work with Java 21 we need to install the OpenJDK 21 on our machine and make it available After this we can configure in Intellij that our project uses java 21 by pointing to use /Library/Java/JavaVirtualMachines/jdk-21 folder as the source for the JDK. 1. Start the dynamodb-init Docker container. 2. Open the "Database" sidebar in IntelliJ and click the plus icon. 3. Select DynamoDB as the data source and fill in with the following details then connect: 5. The table(s) present in the Dockerised DynamoDB should now be visible in the Database sidebar. 6. There will be no items in the table unless you populate it somehow, either using a PPA endpoint, or manually interacting with the database.

## 2. Technology Stack

- **Languages:** Java, Shell
- **Frameworks:** Not detected
- **Runtime:** Not detected
- **Databases:** Not detected
- **Cloud Platforms:** Not detected
- **Containers:** Docker, Docker Compose
- **Kubernetes Helm Terraform:** Not detected
- **Ci Cd:** GitHub Actions
- **Testing Tools:** Not detected
- **Monitoring Observability:** Not detected
- **Important Core Libraries:** Not detected

## 3. Repository Scan and Engineering Artifacts

- **Important files:** .github/workflows/application-config-apply.yaml, .github/workflows/certificate-checker.yaml, .github/workflows/jumpbox.yaml, .github/workflows/kafka.yaml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/nft.yaml, .github/workflows/pr-reviews.yaml, .github/workflows/retry-failed-jobs.yaml, .github/workflows/service-deploy-int-nft.yaml, .github/workflows/service-deploy-stable-int-nbcu.yaml, .github/workflows/service-deploy-stable-int-skyglobal.yaml, .github/workflows/service-extended-test.yaml, .github/workflows/service-main.yaml, .github/workflows/service-p2p-Nbcu.yaml, .github/workflows/service-p2p-SkyGlobal.yaml, .github/workflows/service-p2p-Summer.yaml, .github/workflows/status-check.yaml, .github/workflows/stubs.yaml, README.md

- **Configuration:** .applications/service/application.yaml, .jira/config.yml, config/docker/hbo-private-keys/.gitignore, config/docker/hbo-private-keys/B3RUP5NS2D.pem, config/docker/hbo-private-keys/GN79EMSN1Z.pem, config/docker/hbo-private-keys/README.md, config/docker/hbo-private-keys/generate-test-keys.sh, config/docker/hbo-public-keys/H868bEXwVwDfiYYetGbQ5BEgC0TQY6tHzzzPX0zpWc5.jwk, config/docker/kafka/primary.notification.keystore.jks, config/docker/kafka/primary.notification.truststore.jks, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_4xx.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_5xx.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_customer-not-found.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_invalid-request.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_product-change-pending.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_undocumented.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_unique-request-id.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_success.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_success_already-processed.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_success_default.json, config/mappings/boku/cancelEntitlement/slow-deps/boku_cancel-entitlement_success_slow_dep.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_4xx.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_5xx.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_5xx_timeout.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_concurrent-request.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_duplicate-service.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_internal-error.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_invalid-request.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_product-change-pending.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_product-contigency-unmet.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_rate-limit-reached.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_service-overlap.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_undocumented.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_unique-customer-id.json, config/mappings/boku/createEntitlement/boku_create-entitlement_failure_unique-request-id.json, config/mappings/boku/createEntitlement/boku_create-entitlement_success-expired.json, config/mappings/boku/createEntitlement/boku_create-entitlement_success.json, config/mappings/boku/createEntitlement/boku_create-entitlement_success_already-processed.json, config/mappings/boku/createEntitlement/boku_create-entitlement_success_default.json, config/mappings/boku/createEntitlement/slow-deps/boku_create-entitlement_success_slow.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_failure_4xx.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_failure_5xx.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_failure_already-claimed.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_failure_customer-not-found.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_failure_invalid-request.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_failure_product-change-pending.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_failure_undocumented.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_failure_unique-request-id.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_success-generate.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_success-generate_generic.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_success-resend-generic.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_success-resend.json, config/mappings/boku/remintDeeplinkToken/boku_remint-deeplink-token_success_already-processed.json, config/mappings/boku/remintDeeplinkToken/slow-dep/boku_remint-deeplink-token_success_slow.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_4xx.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_5xx.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_already_cancelled.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_concurrent-request.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_customer_not_found.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_duplicate-service.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_incompatible_product_change.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_internal-error.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_invalid-request.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_linked-customer-ineligible.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_product-change-pending.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_product-contigency-unmet.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_product_not_provisioned.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_rate-limit-reached.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_service-overlap.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_unique-customer-id.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_failure_unique-request-id.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_success.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_success_already-processed.json, config/mappings/boku/updateEntitlement/boku_update-entitlement_success_default.json, config/mappings/boku/updateEntitlement/slow-dep/boku_update-entitlement_success_slow.json, config/mappings/hbo/complete/hbo_complete_success_gb.json, config/mappings/hbo/complete/hbo_complete_success_ie.json, config/mappings/hbo/complete/slow-deps/hbo_complete_success_gb_slow.json, config/mappings/hbo/event/hbo_event_cancel_success_default.json, config/mappings/hbo/event/hbo_event_provision_connection_failure.json, config/mappings/hbo/event/hbo_event_provision_failure_400_unimplemented_error_code.json, config/mappings/hbo/event/hbo_event_provision_failure_500_service_regression.json, config/mappings/hbo/event/hbo_event_provision_failure_500_unimplemented_error_code.json, config/mappings/hbo/event/hbo_event_provision_failure_505_unimplemented_http_status.json, config/mappings/hbo/event/hbo_event_provision_failure_bad_request.json, config/mappings/hbo/event/hbo_event_provision_failure_invalid_event.json, config/mappings/hbo/event/hbo_event_provision_failure_invalid_product.json, config/mappings/hbo/event/hbo_event_provision_failure_invalid_user.json, config/mappings/hbo/event/hbo_event_provision_failure_product_conflict.json, config/mappings/hbo/event/hbo_event_provision_failure_service_regression.json, config/mappings/hbo/event/hbo_event_provision_failure_socket_timeout.json, config/mappings/hbo/event/hbo_event_provision_failure_timeout.json, config/mappings/hbo/event/hbo_event_provision_failure_unauthorised_user.json, config/mappings/hbo/event/hbo_event_provision_success_default.json, config/mappings/hbo/event/slow-deps/hbo_event_cancel_success_slow.json, config/mappings/hbo/event/slow-deps/hbo_event_provision_success_slow.json, config/mappings/tracing/tracing.json, service/func/src/test/java/uk/sky/commerce/ppa/config/HboTestConfig.java, service/func/src/test/java/uk/sky/commerce/ppa/config/TestContextConfig.java, service/func/src/test/java/uk/sky/commerce/ppa/config/TestExecutionContext.java, service/func/src/test/java/uk/sky/commerce/ppa/config/WiremockClientConfig.java, service/func/src/test/resources/application.yml, service/src/main/java/uk/sky/commerce/ppa/config/EventListenerRequestDeserializer.java, service/src/main/java/uk/sky/commerce/ppa/config/FilterConfig.java, service/src/main/java/uk/sky/commerce/ppa/config/InitResourceEndpointConfig.java, service/src/main/java/uk/sky/commerce/ppa/config/ObfuscatedIdGeneratorConfiguration.java, service/src/main/java/uk/sky/commerce/ppa/config/ProvisionRequestDeserializer.java, service/src/main/java/uk/sky/commerce/ppa/database/config/PpaTableResolverConfig.java, service/src/main/java/uk/sky/commerce/ppa/kafka/producer/config/AuthConfigMaskPasswordSerializer.java, service/src/main/java/uk/sky/commerce/ppa/kafka/producer/config/CommerceKafkaProducerAuthConfiguration.java, service/src/main/java/uk/sky/commerce/ppa/kafka/producer/config/CommerceKafkaProducerConfiguration.java, service/src/main/java/uk/sky/commerce/ppa/kafka/producer/config/CommerceKafkaProducerConfigurations.java, service/src/main/java/uk/sky/commerce/ppa/kafka/producer/config/CommerceKafkaProducerHealthCheckConfiguration.java, service/src/main/java/uk/sky/commerce/ppa/validation/config/ValidationConfig.java, service/src/main/resources/application.yml, service/src/test/java/uk/sky/commerce/ppa/config/EventListenerRequestDeserializerTest.java, service/src/test/java/uk/sky/commerce/ppa/config/InitResourceEndpointConfigTest.java, service/src/test/java/uk/sky/commerce/ppa/config/ProvisionRequestDeserializerTest.java, service/src/test/java/uk/sky/commerce/ppa/config/TestContextConfig.java, service/src/test/java/uk/sky/commerce/ppa/database/config/AwsConfigTest.java
- **Docker:** docker-compose.yaml, service/Dockerfile, service/nft/Dockerfile
- **Kubernetes Helm:** Not detected
- **Terraform:** Not detected
- **Ci Cd:** .github/workflows/application-config-apply.yaml, .github/workflows/certificate-checker.yaml, .github/workflows/jumpbox.yaml, .github/workflows/kafka.yaml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/nft.yaml, .github/workflows/pr-reviews.yaml, .github/workflows/retry-failed-jobs.yaml, .github/workflows/service-deploy-int-nft.yaml, .github/workflows/service-deploy-stable-int-nbcu.yaml, .github/workflows/service-deploy-stable-int-skyglobal.yaml, .github/workflows/service-extended-test.yaml, .github/workflows/service-main.yaml, .github/workflows/service-p2p-Nbcu.yaml, .github/workflows/service-p2p-SkyGlobal.yaml, .github/workflows/service-p2p-Summer.yaml, .github/workflows/status-check.yaml, .github/workflows/stubs.yaml
- **Api Specs:** sas-openapi.json
- **Documentation:** README.md, certificate-checker/readme.MD, config/docker/hbo-private-keys/README.md, service/func/README.md, service/src/test/resources/test-keys/README.md

## 4. Main Components and Code Structure

### service
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 266 analyzed core files under service/

### config
Configuration
**Evidence:** 95 analyzed core files under config/

### ppa-bruno
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 30 analyzed core files under ppa-bruno/

### .github
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 24 analyzed core files under .github/

### stubs
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 9 analyzed core files under stubs/

### .applications
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 9 analyzed core files under .applications/

### spec
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 6 analyzed core files under spec/

### gradle
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 3 analyzed core files under gradle/

### certificate-checker
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 3 analyzed core files under certificate-checker/

### commons
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 3 analyzed core files under commons/

### jumpbox
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 2 analyzed core files under jumpbox/

### kafka
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 2 analyzed core files under kafka/

### dynamodb
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 1 analyzed core files under dynamodb/

### .jira
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 1 analyzed core files under .jira/

## 5. Code Architecture

- **Architecture Style:** Modular repository architecture
- **Architecture Explanation:** The repository follows a modular repository architecture. Static analysis identified 14 major structural component areas, 0 executable/package entry points, and 0 repository-local dependency relationships. The architecture below is generated from source layout, imports, symbols, package metadata and executable entry points; the local LLM is used only to explain these facts in repository-specific language.

### Layers / Modules

| Layer / Module | Description | Evidence |
| --- | --- | --- |
| service | Top-level source/component area; semantic responsibility refined by local LLM | 266 analyzed core files under service/ |
| config | Configuration | 95 analyzed core files under config/ |
| ppa-bruno | Top-level source/component area; semantic responsibility refined by local LLM | 30 analyzed core files under ppa-bruno/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 24 analyzed core files under .github/ |
| stubs | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under stubs/ |
| .applications | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under .applications/ |
| spec | Top-level source/component area; semantic responsibility refined by local LLM | 6 analyzed core files under spec/ |
| gradle | Top-level source/component area; semantic responsibility refined by local LLM | 3 analyzed core files under gradle/ |
| certificate-checker | Top-level source/component area; semantic responsibility refined by local LLM | 3 analyzed core files under certificate-checker/ |
| commons | Top-level source/component area; semantic responsibility refined by local LLM | 3 analyzed core files under commons/ |
| jumpbox | Top-level source/component area; semantic responsibility refined by local LLM | 2 analyzed core files under jumpbox/ |
| kafka | Top-level source/component area; semantic responsibility refined by local LLM | 2 analyzed core files under kafka/ |
| dynamodb | Top-level source/component area; semantic responsibility refined by local LLM | 1 analyzed core files under dynamodb/ |
| .jira | Top-level source/component area; semantic responsibility refined by local LLM | 1 analyzed core files under .jira/ |

### Entry Points

_Not detected._

### Major Components

| Component | Responsibility | Evidence |
| --- | --- | --- |
| service | Top-level source/component area; semantic responsibility refined by local LLM | 266 analyzed core files under service/ |
| config | Configuration | 95 analyzed core files under config/ |
| ppa-bruno | Top-level source/component area; semantic responsibility refined by local LLM | 30 analyzed core files under ppa-bruno/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 24 analyzed core files under .github/ |
| stubs | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under stubs/ |
| .applications | Top-level source/component area; semantic responsibility refined by local LLM | 9 analyzed core files under .applications/ |
| spec | Top-level source/component area; semantic responsibility refined by local LLM | 6 analyzed core files under spec/ |
| gradle | Top-level source/component area; semantic responsibility refined by local LLM | 3 analyzed core files under gradle/ |
| certificate-checker | Top-level source/component area; semantic responsibility refined by local LLM | 3 analyzed core files under certificate-checker/ |
| commons | Top-level source/component area; semantic responsibility refined by local LLM | 3 analyzed core files under commons/ |
| jumpbox | Top-level source/component area; semantic responsibility refined by local LLM | 2 analyzed core files under jumpbox/ |
| kafka | Top-level source/component area; semantic responsibility refined by local LLM | 2 analyzed core files under kafka/ |
| dynamodb | Top-level source/component area; semantic responsibility refined by local LLM | 1 analyzed core files under dynamodb/ |
| .jira | Top-level source/component area; semantic responsibility refined by local LLM | 1 analyzed core files under .jira/ |

### Component Relationships

_Not detected._

### Configuration Model

Repository contains explicit configuration artifacts: .applications/service/application.yaml, .jira/config.yml, config/docker/hbo-private-keys/.gitignore, config/docker/hbo-private-keys/B3RUP5NS2D.pem, config/docker/hbo-private-keys/GN79EMSN1Z.pem, config/docker/hbo-private-keys/README.md, config/docker/hbo-private-keys/generate-test-keys.sh, config/docker/hbo-public-keys/H868bEXwVwDfiYYetGbQ5BEgC0TQY6tHzzzPX0zpWc5.jwk, config/docker/kafka/primary.notification.keystore.jks, config/docker/kafka/primary.notification.truststore.jks, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_4xx.json, config/mappings/boku/cancelEntitlement/boku_cancel-entitlement_failure_5xx.json.

### Extension Points

- gradle/plugins/common.gradle
- service/gradle-plugins/app-promotion-plugin.gradle
- service/gradle-plugins/change-request-plugin.gradle
- service/gradle-plugins/deployments.gradle
- service/gradle-plugins/deployments/nbcu/change-request-plugin.gradle
- service/gradle-plugins/deployments/nbcu/us-east-2/app-promotion-plugin.gradle
- service/gradle-plugins/deployments/nbcu/us-east-2/deployments.gradle
- service/gradle-plugins/deployments/nbcu/us-west-2/app-promotion-plugin.gradle
- service/gradle-plugins/deployments/nbcu/us-west-2/deployments.gradle
- service/gradle-plugins/deployments/skyglobal/change-request-plugin.gradle
- service/gradle-plugins/deployments/skyglobal/eu-central-1/app-promotion-plugin.gradle
- service/gradle-plugins/deployments/skyglobal/eu-central-1/deployments.gradle
- service/gradle-plugins/deployments/skyglobal/eu-west-1/app-promotion-plugin.gradle
- service/gradle-plugins/deployments/skyglobal/eu-west-1/deployments.gradle
- service/gradle-plugins/deployments/summer/change-request-plugin.gradle
- service/gradle-plugins/deployments/summer/eu-central-1/app-promotion-plugin.gradle
- service/gradle-plugins/deployments/summer/eu-central-1/deployments.gradle
- service/gradle-plugins/deployments/summer/us-east-2/deployments.gradle
- service/gradle-plugins/release.gradle
- service/gradle-plugins/sonarqube.gradle
- service/nft/gradle-plugins/deployments.gradle
- service/nft/gradle-plugins/deployments/nbcu/deployments.gradle
- service/nft/gradle-plugins/deployments/nbcu/us-west-2/deployments.gradle
- service/nft/gradle-plugins/deployments/skyglobal/deployments.gradle
- service/nft/gradle-plugins/deployments/skyglobal/eu-central-1/deployments.gradle

### Deployment Model

Docker

### Architecture Data / Control Flow

1. No single executable entry point was found; this repository is likely consumed as a library/framework or exposes multiple integration entry points.
2. Configuration artifacts influence component initialization and runtime behavior.
3. Core components process requests/commands/events through repository modules and return results to the caller or downstream integration.

## 6. Overall Code Flow

- **Code Flow Analysis Status:** Deterministic static code-flow fallback (--skip-llm)

This section explains the repository flow in simple execution order. It separates the main runtime from independent automation/tooling paths and only uses code/source evidence found in the repository.

### Flow Overview

The repository runtime starts from its executable entry point, loads configuration and infrastructure dependencies, registers production routes, and starts the service. Each request then follows the statically resolved handler -> use case/service -> repository -> DAL/client path where such a chain is proven. Persistence operations are shown only when directly detected in source. The service closes through its graceful shutdown path when one is present.

### Application Startup Flow

#### Step 1: Load runtime configuration

The application uses the detected configuration files during startup. Configuration values control later runtime initialization; values not proven from source are not guessed.

**Code / files involved:**
- `.applications/service/application.yaml`
- `.jira/config.yml`
- `config/docker/hbo-private-keys/.gitignore`
- `config/docker/hbo-private-keys/B3RUP5NS2D.pem`
- `config/docker/hbo-private-keys/GN79EMSN1Z.pem`
- `config/docker/hbo-private-keys/README.md`
- `config/docker/hbo-private-keys/generate-test-keys.sh`
- `config/docker/hbo-public-keys/H868bEXwVwDfiYYetGbQ5BEgC0TQY6tHzzzPX0zpWc5.jwk`
- `config/docker/kafka/primary.notification.keystore.jks`
- `config/docker/kafka/primary.notification.truststore.jks`

**What happens next:** Validated runtime settings are available to the bootstrap code.

**Evidence:** .applications/service/application.yaml, .jira/config.yml, config/docker/hbo-private-keys/.gitignore, config/docker/hbo-private-keys/B3RUP5NS2D.pem, config/docker/hbo-private-keys/GN79EMSN1Z.pem, config/docker/hbo-private-keys/README.md, config/docker/hbo-private-keys/generate-test-keys.sh, config/docker/hbo-public-keys/H868bEXwVwDfiYYetGbQ5BEgC0TQY6tHzzzPX0zpWc5.jwk, config/docker/kafka/primary.notification.keystore.jks, config/docker/kafka/primary.notification.truststore.jks

### Static Call / Module Paths

The paths below are the exact callable/import chains that static analysis could prove. They support the simplified flow above.

No complete callable chain was statically provable for this repository.

## 7. Dependencies and Compatibility

Dependencies are grouped by scope. Example/test/documentation dependencies do not contaminate the core technology stack.

## 8. Tests and Coverage

- **Testing frameworks:** Not detected
- **Test files detected:** 182
- **Coverage status:** Actual coverage result not found
- **Coverage percentage:** Not available
- **Coverage source:** Not available

## 9. Production Internal APIs

_Test/mock/example routes are excluded._

| Method | Endpoint | Handler | Component | Source File |
| --- | --- | --- | --- | --- |
| GET | /household/{householdId} | Not available | ProvisionedPartnerInternalController | service/src/main/java/uk/sky/commerce/ppa/controller/ProvisionedPartnerInternalController.java |
| GET | /external-account/{externalAccountId} | Not available | ProvisionedPartnerInternalController | service/src/main/java/uk/sky/commerce/ppa/controller/ProvisionedPartnerInternalController.java |
| POST | /integration-api/v2/event/{partnerId} | Not available | HBOEventClient | service/src/main/java/uk/sky/commerce/ppa/http/client/hbo/sendevent/client/HBOEventClient.java |
| GET | /broker/complete/{partnerId}/{brandId} | Not available | HBOCompleteClient | service/src/main/java/uk/sky/commerce/ppa/http/client/hbo/complete/client/HBOCompleteClient.java |

## 10. Production External API and Integration Calls

_Test/mock/example calls are excluded._

_Not detected._

## 11. Main Use Cases

No high-level use cases were returned by the local LLM.

## 12. Analysis Limitations

- Local LLM skipped; deterministic architecture and detailed static code flow are still reported.
