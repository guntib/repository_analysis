# Repository Intelligent Analysis Report

## 1. Repository Summary

- **Repository:** bragi-commons
- **Source:** https://github.com/NBCUDTC/bragi-commons.git
- **Source Type:** GitHub
- **Repository Type:** Application / Service / Library Repository
- **Files Analyzed:** 830
- **Local LLM Status:** Skipped by command line

### What the Application / Repository Does

Commons - Module that include common code for the other modules / projects Logs - Module to include logging related common code / logic Metrics - Module with the common prometheus metrics Resilience - Resilience commons (eg: healthcheck endpoint, circuit breakers. etc) Mocks - Mocks (eg: wiremock for downstream) Security - Module with security helpers, eg: Sky Signature Header generator & validator Sky OTT UserToken Header generator & validator Tracing - OTel-compliant span naming, Sky tenant enrichment and MDC alignment for HTTP, Cassandra, Kafka, MongoDB and Redis Releases: https://nexus.ovp.mgmt-aws.ottlocal.sky/nexus/content/repositories/sky-releases/uk/sky/commerce/bragi/commons/ Snapshots: https://nexus.ovp.mgmt-aws.ottlocal.sky/nexus/content/repositories/sky-snapshots/uk/sky/commerce/bragi/commons/ https://jenkins-bragi.tools.cosmic.sky/job/bragi/job/bragi-commons/ Below is the internal dependency tree for our own libraries. Ideally, they would always be in sync. This means that if you had to make changes to the commons library, you would update this dependency down the tree for all libraries that depend on it. This ensures that we're always using the same version and avoidi

### Repository Summary

Commons - Module that include common code for the other modules / projects Logs - Module to include logging related common code / logic Metrics - Module with the common prometheus metrics Resilience - Resilience commons (eg: healthcheck endpoint, circuit breakers. etc) Mocks - Mocks (eg: wiremock for downstream) Security - Module with security helpers, eg: Sky Signature Header generator & validator Sky OTT UserToken Header generator & validator Tracing - OTel-compliant span naming, Sky tenant enrichment and MDC alignment for HTTP, Cassandra, Kafka, MongoDB and Redis Releases: https://nexus.ovp.mgmt-aws.ottlocal.sky/nexus/content/repositories/sky-releases/uk/sky/commerce/bragi/commons/ Snapshots: https://nexus.ovp.mgmt-aws.ottlocal.sky/nexus/content/repositories/sky-snapshots/uk/sky/commerce/bragi/commons/ https://jenkins-bragi.tools.cosmic.sky/job/bragi/job/bragi-commons/ Below is the internal dependency tree for our own libraries. Ideally, they would always be in sync. This means that if you had to make changes to the commons library, you would update this dependency down the tree for all libraries that depend on it. This ensures that we're always using the same version and avoidi

## 2. Technology Stack

- **Languages:** Java, Python, Kotlin, Shell, TypeScript, JavaScript
- **Frameworks:** React
- **Runtime:** Not detected
- **Databases:** Not detected
- **Cloud Platforms:** Not detected
- **Containers:** Docker, Docker Compose
- **Kubernetes Helm Terraform:** Not detected
- **Ci Cd:** GitHub Actions
- **Testing Tools:** Jest
- **Monitoring Observability:** Not detected
- **Important Core Libraries:** @tanstack/react-table, bootstrap, debug, luxon, react, react-bootstrap, react-router, react-toastify

## 3. Repository Scan and Engineering Artifacts

- **Important files:** .github/workflows/1101-backoffice-commons.yaml, .github/workflows/1199-backoffice-commons-pr.yaml, .github/workflows/1201-build-conventions-plugin.yaml, .github/workflows/1299-build-conventions-plugin-pr.yaml, .github/workflows/1301-commons.yaml, .github/workflows/1399-commons-pr.yaml, .github/workflows/1401-dependencies.yaml, .github/workflows/1499-dependencies-pr.yaml, .github/workflows/1501-kafka.yaml, .github/workflows/1599-kafka-pr.yaml, .github/workflows/1601-local-initializer.yaml, .github/workflows/1699-local-initializer-pr.yaml, .github/workflows/1701-logs.yaml, .github/workflows/1799-logs-pr.yaml, .github/workflows/1801-metrics.yaml, .github/workflows/1899-metrics-pr.yaml, .github/workflows/1901-mongo.yaml, .github/workflows/1999-mongo-pr.yaml, .github/workflows/2001-resilience.yaml, .github/workflows/2099-resilience-pr.yaml, .github/workflows/2101-rest-client.yaml, .github/workflows/2199-rest-client-pr.yaml, .github/workflows/2201-security.yaml, .github/workflows/2299-security-pr.yaml, .github/workflows/2301-wiremock.yaml, .github/workflows/2399-wiremock-pr.yaml, .github/workflows/9001-application-config-apply.yaml, .github/workflows/bernabot-check-outcomes.yml, .github/workflows/bernabot-feedback.yml, .github/workflows/bernabot-housekeeper-feedback.yml, .github/workflows/bernabot-housekeeper.yml, .github/workflows/bernabot-incidents.yml, .github/workflows/bernabot-learnings.yml, .github/workflows/bernabot-pr.yaml, .github/workflows/bernabot-resolve.yml, .github/workflows/bernabot-skills.yml, .github/workflows/bernabot.yml, .github/workflows/bernacop.yml, .github/workflows/bragi-agent-config-pr.yaml, .github/workflows/changelog_suggestion.yml, .github/workflows/knowledge-api-smoke-test.yml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/pr_build.yml, README.md

- **Configuration:** commons/src/main/java/uk/sky/commerce/bragi/commons/abtesting/config/ABTestConfiguration.java, commons/src/main/java/uk/sky/commerce/bragi/commons/config/ConfigCopyUtils.java, commons/src/test/java/uk/sky/commerce/bragi/commons/config/ConfigCopyUtilsTest.java, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/AxionReleaseConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ConfigUtils.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/DependencyLockingConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/DeploymentConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/GitConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ImagePublishingConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/JacocoConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/NftTestsReportingConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/OpenApiConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/SnapshotDependencyCheckConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/SonarQubeConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/SpotlessConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/cucumber/CucumberTestsConfig.groovy, gradle-plugins/build-conventions-plugin/src/test/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/AxionReleaseConfigFunctionalSpec.groovy, gradle-plugins/build-conventions-plugin/src/test/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/AxionReleaseConfigSpec.groovy, gradle-plugins/build-conventions-plugin/src/test/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/FunctionalSpecTrait.groovy, gradle-plugins/build-conventions-plugin/src/test/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/GitConfigFunctionalSpec.groovy, gradle-plugins/build-conventions-plugin/src/test/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/GitConfigSpec.groovy, gradle-plugins/build-conventions-plugin/src/test/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ImagePublishingConfigSpec.groovy, gradle-plugins/build-conventions-plugin/src/test/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/SpotlessConfigFunctionalSpec.groovy, gradle-plugins/build-conventions-plugin/src/test/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/SpotlessConfigSpec.groovy, resilience/src/main/java/uk/sky/commerce/bragi/commons/resilience/health/check/config/HealthcheckConfig.kt, resilience/src/main/java/uk/sky/commerce/bragi/commons/resilience/integration/check/config/DefaultDownstreamConfigsProvider.kt, resilience/src/main/java/uk/sky/commerce/bragi/commons/resilience/integration/check/config/DefaultRestClientProperties.kt, resilience/src/main/java/uk/sky/commerce/bragi/commons/resilience/integration/check/config/DownstreamConfigs.kt, resilience/src/main/java/uk/sky/commerce/bragi/commons/resilience/integration/check/config/DownstreamConfigsProvider.kt, resilience/src/main/java/uk/sky/commerce/bragi/commons/resilience/integration/check/config/IntegrationCheckConfig.kt, resilience/src/test/java/uk/sky/commerce/bragi/commons/resilience/integration/check/config/DefaultDownstreamConfigsProviderTest.kt, resilience/src/test/java/uk/sky/commerce/bragi/commons/resilience/integration/check/config/DownstreamConfigsTest.kt, rest-client/src/main/java/uk/sky/commerce/bragi/commons/rest/config/RestClientProperties.java, rest-client/src/main/java/uk/sky/commerce/bragi/commons/rest/config/RestClientPropertiesPerTenant.java, rest-client/src/main/java/uk/sky/commerce/bragi/commons/rest/resilience/config/AbstractResiliencyPatternProperties.java, rest-client/src/main/java/uk/sky/commerce/bragi/commons/rest/resilience/config/BulkheadResiliencyPatternProperties.java, rest-client/src/main/java/uk/sky/commerce/bragi/commons/rest/resilience/config/CircuitBreakerResiliencyPatternProperties.java, rest-client/src/main/java/uk/sky/commerce/bragi/commons/rest/resilience/config/RateLimiterResiliencyPatternProperties.java, rest-client/src/main/java/uk/sky/commerce/bragi/commons/rest/resilience/config/ResilienceProperties.java, rest-client/src/main/java/uk/sky/commerce/bragi/commons/rest/resilience/config/RetryResiliencyPatternProperties.java
- **Docker:** docker-compose.yaml, mocks/kafka/Dockerfile, mocks/mongo/Dockerfile, mocks/wiremock/Dockerfile
- **Kubernetes Helm:** Not detected
- **Terraform:** Not detected
- **Ci Cd:** .github/workflows/1101-backoffice-commons.yaml, .github/workflows/1199-backoffice-commons-pr.yaml, .github/workflows/1201-build-conventions-plugin.yaml, .github/workflows/1299-build-conventions-plugin-pr.yaml, .github/workflows/1301-commons.yaml, .github/workflows/1399-commons-pr.yaml, .github/workflows/1401-dependencies.yaml, .github/workflows/1499-dependencies-pr.yaml, .github/workflows/1501-kafka.yaml, .github/workflows/1599-kafka-pr.yaml, .github/workflows/1601-local-initializer.yaml, .github/workflows/1699-local-initializer-pr.yaml, .github/workflows/1701-logs.yaml, .github/workflows/1799-logs-pr.yaml, .github/workflows/1801-metrics.yaml, .github/workflows/1899-metrics-pr.yaml, .github/workflows/1901-mongo.yaml, .github/workflows/1999-mongo-pr.yaml, .github/workflows/2001-resilience.yaml, .github/workflows/2099-resilience-pr.yaml, .github/workflows/2101-rest-client.yaml, .github/workflows/2199-rest-client-pr.yaml, .github/workflows/2201-security.yaml, .github/workflows/2299-security-pr.yaml, .github/workflows/2301-wiremock.yaml, .github/workflows/2399-wiremock-pr.yaml, .github/workflows/9001-application-config-apply.yaml, .github/workflows/bernabot-check-outcomes.yml, .github/workflows/bernabot-feedback.yml, .github/workflows/bernabot-housekeeper-feedback.yml, .github/workflows/bernabot-housekeeper.yml, .github/workflows/bernabot-incidents.yml, .github/workflows/bernabot-learnings.yml, .github/workflows/bernabot-pr.yaml, .github/workflows/bernabot-resolve.yml, .github/workflows/bernabot-skills.yml, .github/workflows/bernabot.yml, .github/workflows/bernacop.yml, .github/workflows/bragi-agent-config-pr.yaml, .github/workflows/changelog_suggestion.yml, .github/workflows/knowledge-api-smoke-test.yml, .github/workflows/locstat-preserve-stats-on-merge.yml, .github/workflows/locstat-verify-notes.yml, .github/workflows/pr_build.yml
- **Api Specs:** gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/OpenApiConfig.groovy, sas-openapi.json
- **Documentation:** .github/scripts/bernabot/README.md, .github/scripts/bernacop/README.md, README.md, backoffice-commons/README.md, bragi-agent-config/README.md, bragi-agent-config/plugins/bernabot-plugin/README.md, bragi-agent-config/plugins/bragi-agent-skills/README.md, bragi-agent-config/plugins/bragi-agent-skills/skills/run-functional-tests/evals/README.md, bragi-agent-config/plugins/bragi-agent-skills/template/evals/README.md, bragi-agent-config/plugins/recruiting-plugin/README.md, bragi-agent-config/plugins/recruiting-plugin/skills/homework-reviewer/README.md, bragi-agent-config/plugins/scrum-plugin/README.md, commons/README.md, dependencies/README.md, gradle-plugins/build-conventions-plugin/README.md, gradle-plugins/local-initializer/README.md, logs/README.md, metrics/README.md, mocks/README.md, resilience/README.md, rest-client/README.md, security/README.md, tracing/README.md

## 4. Main Components and Code Structure

### .github
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 147 analyzed core files under .github/

### bragi-agent-config
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 107 analyzed core files under bragi-agent-config/

### commons
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 60 analyzed core files under commons/

### gradle-plugins
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 52 analyzed core files under gradle-plugins/

### rest-client
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 41 analyzed core files under rest-client/

### security
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 41 analyzed core files under security/

### backoffice-commons
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 40 analyzed core files under backoffice-commons/

### mocks
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 38 analyzed core files under mocks/

### resilience
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 34 analyzed core files under resilience/

### tracing
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 25 analyzed core files under tracing/

### metrics
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 16 analyzed core files under metrics/

### logs
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 16 analyzed core files under logs/

### .applications
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 15 analyzed core files under .applications/

### logs-common
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 14 analyzed core files under logs-common/

### dependencies
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 6 analyzed core files under dependencies/

## 5. Code Architecture

- **Architecture Style:** Modular Python application architecture
- **Architecture Explanation:** The repository follows a modular python application architecture. Static analysis identified 15 major structural component areas, 42 executable/package entry points, and 19 repository-local dependency relationships. The architecture below is generated from source layout, imports, symbols, package metadata and executable entry points; the local LLM is used only to explain these facts in repository-specific language.

### Layers / Modules

| Layer / Module | Description | Evidence |
| --- | --- | --- |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 147 analyzed core files under .github/ |
| bragi-agent-config | Top-level source/component area; semantic responsibility refined by local LLM | 107 analyzed core files under bragi-agent-config/ |
| commons | Top-level source/component area; semantic responsibility refined by local LLM | 60 analyzed core files under commons/ |
| gradle-plugins | Top-level source/component area; semantic responsibility refined by local LLM | 52 analyzed core files under gradle-plugins/ |
| rest-client | Top-level source/component area; semantic responsibility refined by local LLM | 41 analyzed core files under rest-client/ |
| security | Top-level source/component area; semantic responsibility refined by local LLM | 41 analyzed core files under security/ |
| backoffice-commons | Top-level source/component area; semantic responsibility refined by local LLM | 40 analyzed core files under backoffice-commons/ |
| mocks | Top-level source/component area; semantic responsibility refined by local LLM | 38 analyzed core files under mocks/ |
| resilience | Top-level source/component area; semantic responsibility refined by local LLM | 34 analyzed core files under resilience/ |
| tracing | Top-level source/component area; semantic responsibility refined by local LLM | 25 analyzed core files under tracing/ |
| metrics | Top-level source/component area; semantic responsibility refined by local LLM | 16 analyzed core files under metrics/ |
| logs | Top-level source/component area; semantic responsibility refined by local LLM | 16 analyzed core files under logs/ |
| .applications | Top-level source/component area; semantic responsibility refined by local LLM | 15 analyzed core files under .applications/ |
| logs-common | Top-level source/component area; semantic responsibility refined by local LLM | 14 analyzed core files under logs-common/ |
| dependencies | Top-level source/component area; semantic responsibility refined by local LLM | 6 analyzed core files under dependencies/ |

### Entry Points

| Type | Symbol / Command | Source File |
| --- | --- | --- |
| Python executable entry point | .github.scripts.changelog.update | .github/scripts/changelog/update.py |
| Python executable entry point | .github.scripts.changelog.check | .github/scripts/changelog/check.py |
| Python executable entry point | .github.scripts.changelog.post_result | .github/scripts/changelog/post_result.py |
| Python executable entry point | .github.scripts.changelog.create_review | .github/scripts/changelog/create_review.py |
| Python executable entry point | .github.scripts.changelog.prepare | .github/scripts/changelog/prepare.py |
| Python executable entry point | .github.scripts.utils.check_permissions | .github/scripts/utils/check_permissions.py |
| Python executable entry point | .github.scripts.utils.check_trigger | .github/scripts/utils/check_trigger.py |
| Python executable entry point | .github.scripts.bernabot.generate_token | .github/scripts/bernabot/generate_token.py |
| Python executable entry point | .github.scripts.bernacop.test_bernacop | .github/scripts/bernacop/test_bernacop.py |
| Python executable entry point | .github.scripts.bernacop.generate_token | .github/scripts/bernacop/generate_token.py |
| Python executable entry point | .github.scripts.bernacop.bernacop | .github/scripts/bernacop/bernacop.py |
| Python executable entry point | .github.scripts.bernacop.generate_pages | .github/scripts/bernacop/generate_pages.py |
| Python executable entry point | .github.scripts.bernabot.shared.auth | .github/scripts/bernabot/shared/auth.py |
| Python executable entry point | .github.scripts.bernabot.cli.fetch_incidents | .github/scripts/bernabot/cli/fetch_incidents.py |
| Python executable entry point | .github.scripts.bernabot.cli.investigate_incident | .github/scripts/bernabot/cli/investigate_incident.py |
| Python executable entry point | .github.scripts.bernabot.cli.resolve_issue | .github/scripts/bernabot/cli/resolve_issue.py |
| Python executable entry point | .github.scripts.bernabot.cli.run_housekeeper_job | .github/scripts/bernabot/cli/run_housekeeper_job.py |
| Python executable entry point | .github.scripts.bernabot.cli.scan_learnings | .github/scripts/bernabot/cli/scan_learnings.py |
| Python executable entry point | .github.scripts.bernabot.cli.fetch_housekeeper_feedback_prs | .github/scripts/bernabot/cli/fetch_housekeeper_feedback_prs.py |
| Python executable entry point | .github.scripts.bernabot.cli.generate_skills | .github/scripts/bernabot/cli/generate_skills.py |
| Python executable entry point | .github.scripts.bernabot.cli.check_outcomes | .github/scripts/bernabot/cli/check_outcomes.py |
| Python executable entry point | .github.scripts.bernabot.cli.process_housekeeper_feedback_pr | .github/scripts/bernabot/cli/process_housekeeper_feedback_pr.py |
| Python executable entry point | .github.scripts.bernabot.cli.process_feedback_pr | .github/scripts/bernabot/cli/process_feedback_pr.py |
| Python executable entry point | .github.scripts.bernabot.cli.process_issue | .github/scripts/bernabot/cli/process_issue.py |
| Python executable entry point | .github.scripts.bernabot.cli.skill_up | .github/scripts/bernabot/cli/skill_up.py |
| Python executable entry point | .github.scripts.bernabot.cli.migrate_to_sqlite | .github/scripts/bernabot/cli/migrate_to_sqlite.py |
| Python executable entry point | .github.scripts.bernabot.cli.fetch_issues | .github/scripts/bernabot/cli/fetch_issues.py |
| Python executable entry point | .github.scripts.bernabot.cli.fetch_feedback_prs | .github/scripts/bernabot/cli/fetch_feedback_prs.py |
| Python executable entry point | .github.scripts.bernabot.cli.fetch_housekeeper_jobs | .github/scripts/bernabot/cli/fetch_housekeeper_jobs.py |
| Python executable entry point | .github.scripts.bernabot.cli.show_metrics | .github/scripts/bernabot/cli/show_metrics.py |

### Major Components

| Component | Responsibility | Evidence |
| --- | --- | --- |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 147 analyzed core files under .github/ |
| bragi-agent-config | Top-level source/component area; semantic responsibility refined by local LLM | 107 analyzed core files under bragi-agent-config/ |
| commons | Top-level source/component area; semantic responsibility refined by local LLM | 60 analyzed core files under commons/ |
| gradle-plugins | Top-level source/component area; semantic responsibility refined by local LLM | 52 analyzed core files under gradle-plugins/ |
| rest-client | Top-level source/component area; semantic responsibility refined by local LLM | 41 analyzed core files under rest-client/ |
| security | Top-level source/component area; semantic responsibility refined by local LLM | 41 analyzed core files under security/ |
| backoffice-commons | Top-level source/component area; semantic responsibility refined by local LLM | 40 analyzed core files under backoffice-commons/ |
| mocks | Top-level source/component area; semantic responsibility refined by local LLM | 38 analyzed core files under mocks/ |
| resilience | Top-level source/component area; semantic responsibility refined by local LLM | 34 analyzed core files under resilience/ |
| tracing | Top-level source/component area; semantic responsibility refined by local LLM | 25 analyzed core files under tracing/ |
| metrics | Top-level source/component area; semantic responsibility refined by local LLM | 16 analyzed core files under metrics/ |
| logs | Top-level source/component area; semantic responsibility refined by local LLM | 16 analyzed core files under logs/ |
| .applications | Top-level source/component area; semantic responsibility refined by local LLM | 15 analyzed core files under .applications/ |
| logs-common | Top-level source/component area; semantic responsibility refined by local LLM | 14 analyzed core files under logs-common/ |
| dependencies | Top-level source/component area; semantic responsibility refined by local LLM | 6 analyzed core files under dependencies/ |

### Component Relationships

| From | To | Relationship |
| --- | --- | --- |
| backoffice-commons/src/index.ts | ./components | imports/depends on |
| backoffice-commons/src/components/index.ts | ./layout | imports/depends on |
| backoffice-commons/src/components/index.ts | ./alerts | imports/depends on |
| backoffice-commons/src/components/index.ts | ./input/searchableDropdown | imports/depends on |
| backoffice-commons/src/components/index.ts | ./datatable | imports/depends on |
| backoffice-commons/src/components/input/index.ts | ./searchableDropdown | imports/depends on |
| backoffice-commons/src/components/input/index.ts | ./debouncedInput | imports/depends on |
| backoffice-commons/src/components/layout/index.ts | ./footer | imports/depends on |
| backoffice-commons/src/components/alerts/Alerts.tsx | ./Alerts.types | imports/depends on |
| backoffice-commons/src/components/alerts/index.ts | ./Alerts | imports/depends on |
| backoffice-commons/src/components/datatable/DataTable.tsx | ./DataTable.types.ts | imports/depends on |
| backoffice-commons/src/components/datatable/DataTable.tsx | ../input | imports/depends on |
| backoffice-commons/src/components/datatable/index.ts | ./DataTable.tsx | imports/depends on |
| backoffice-commons/src/components/layout/footer/Footer.tsx | ./Footer.types.ts | imports/depends on |
| backoffice-commons/src/components/layout/footer/index.ts | ./Footer | imports/depends on |
| backoffice-commons/src/components/input/searchableDropdown/index.ts | ./SearchableDropdown.tsx | imports/depends on |
| backoffice-commons/src/components/input/searchableDropdown/SearchableDropdown.tsx | ./SearchableDropdown.types | imports/depends on |
| backoffice-commons/src/components/input/debouncedInput/DebouncedInput.tsx | ./DebouncedInput.types.ts | imports/depends on |
| backoffice-commons/src/components/input/debouncedInput/index.ts | ./DebouncedInput.tsx | imports/depends on |

### Configuration Model

Repository contains explicit configuration artifacts: commons/src/main/java/uk/sky/commerce/bragi/commons/abtesting/config/ABTestConfiguration.java, commons/src/main/java/uk/sky/commerce/bragi/commons/config/ConfigCopyUtils.java, commons/src/test/java/uk/sky/commerce/bragi/commons/config/ConfigCopyUtilsTest.java, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/AxionReleaseConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ConfigUtils.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/DependencyLockingConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/DeploymentConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/GitConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ImagePublishingConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/JacocoConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/NftTestsReportingConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/OpenApiConfig.groovy.

### Extension Points

- .applications/build-conventions-plugin/corepipeline.yaml
- .augment-plugin/marketplace.json
- .github/plugin/marketplace.json
- .github/workflows/1201-build-conventions-plugin.yaml
- .github/workflows/1299-build-conventions-plugin-pr.yaml
- bragi-agent-config/plugins/bernabot-plugin/.augment-plugin/plugin.json
- bragi-agent-config/plugins/bernabot-plugin/AGENTS.md
- bragi-agent-config/plugins/bernabot-plugin/README.md
- bragi-agent-config/plugins/bernabot-plugin/agents/bernabot-conflict-resolver.md
- bragi-agent-config/plugins/bernabot-plugin/agents/bernabot-implementer.md
- bragi-agent-config/plugins/bernabot-plugin/agents/bernabot-reviewer.md
- bragi-agent-config/plugins/bernabot-plugin/build.gradle
- bragi-agent-config/plugins/bernabot-plugin/hooks/enforce-gradle-wait.sh
- bragi-agent-config/plugins/bernabot-plugin/hooks/ensure-node-path.sh
- bragi-agent-config/plugins/bernabot-plugin/hooks/hooks.json
- bragi-agent-config/plugins/bernabot-plugin/hooks/reject-github-api.sh
- bragi-agent-config/plugins/bernabot-plugin/plugin.json
- bragi-agent-config/plugins/bernabot-plugin/rules/bernabot-build-verification.md
- bragi-agent-config/plugins/bernabot-plugin/rules/bernabot-operational-guardrails.md
- bragi-agent-config/plugins/bernabot-plugin/scripts/test-local.sh
- bragi-agent-config/plugins/bragi-agent-skills/.augment-plugin/plugin.json
- bragi-agent-config/plugins/bragi-agent-skills/AGENTS.md
- bragi-agent-config/plugins/bragi-agent-skills/README.md
- bragi-agent-config/plugins/bragi-agent-skills/build.gradle
- bragi-agent-config/plugins/bragi-agent-skills/plugin.json

### Deployment Model

Docker

### Architecture Data / Control Flow

1. Execution begins at the detected repository entry point(s): .github/scripts/changelog/update.py, .github/scripts/changelog/check.py, .github/scripts/changelog/post_result.py, .github/scripts/changelog/create_review.py, .github/scripts/changelog/prepare.py, .github/scripts/utils/check_permissions.py, .github/scripts/utils/check_trigger.py, .github/scripts/bernabot/generate_token.py.
2. Entry modules/packages delegate work through repository-local imports and package dependencies.
3. Static call/import analysis identified concrete execution paths shown in Detailed Code Flows below.
4. Configuration artifacts influence component initialization and runtime behavior.
5. Core components process requests/commands/events through repository modules and return results to the caller or downstream integration.

## 6. Overall Code Flow

- **Code Flow Analysis Status:** Deterministic static code-flow fallback (--skip-llm)

This section explains the repository flow in simple execution order. It separates the main runtime from independent automation/tooling paths and only uses code/source evidence found in the repository.

### Flow Overview

The repository runtime starts from its executable entry point, loads configuration and infrastructure dependencies, registers production routes, and starts the service. Each request then follows the statically resolved handler -> use case/service -> repository -> DAL/client path where such a chain is proven. Persistence operations are shown only when directly detected in source. The service closes through its graceful shutdown path when one is present.

### Application Startup Flow

#### Step 1: Load runtime configuration

The application uses the detected configuration files during startup. Configuration values control later runtime initialization; values not proven from source are not guessed.

**Code / files involved:**
- `commons/src/main/java/uk/sky/commerce/bragi/commons/abtesting/config/ABTestConfiguration.java`
- `commons/src/main/java/uk/sky/commerce/bragi/commons/config/ConfigCopyUtils.java`
- `commons/src/test/java/uk/sky/commerce/bragi/commons/config/ConfigCopyUtilsTest.java`
- `gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/AxionReleaseConfig.groovy`
- `gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ConfigUtils.groovy`
- `gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/DependencyLockingConfig.groovy`
- `gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/DeploymentConfig.groovy`
- `gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/GitConfig.groovy`
- `gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ImagePublishingConfig.groovy`
- `gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/JacocoConfig.groovy`

**What happens next:** Validated runtime settings are available to the bootstrap code.

**Evidence:** commons/src/main/java/uk/sky/commerce/bragi/commons/abtesting/config/ABTestConfiguration.java, commons/src/main/java/uk/sky/commerce/bragi/commons/config/ConfigCopyUtils.java, commons/src/test/java/uk/sky/commerce/bragi/commons/config/ConfigCopyUtilsTest.java, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/AxionReleaseConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ConfigUtils.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/DependencyLockingConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/DeploymentConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/GitConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/ImagePublishingConfig.groovy, gradle-plugins/build-conventions-plugin/src/main/groovy/uk/sky/commerce/bragi/gradle/plugins/buildconventions/config/JacocoConfig.groovy

### Static Call / Module Paths

The paths below are the exact callable/import chains that static analysis could prove. They support the simplified flow above.

#### Python control flow from main
- **Entry Point:** .github.scripts.changelog.update.main
- **Ordered Static Flow:**
  1. `.github.scripts.changelog.update.main`
  2. `.github.scripts.changelog.update.get_changed_modules`
- **Evidence:** Static AST self/local function call graph

#### Python control flow from main
- **Entry Point:** .github.scripts.changelog.check.main
- **Ordered Static Flow:**
  1. `.github.scripts.changelog.check.main`
  2. `.github.scripts.changelog.check.has_skip_label`
- **Evidence:** Static AST self/local function call graph

#### Python control flow from main
- **Entry Point:** .github.scripts.changelog.post_result.main
- **Ordered Static Flow:**
  1. `.github.scripts.changelog.post_result.main`
  2. `.github.scripts.changelog.post_result.find_changelog_review`
- **Evidence:** Static AST self/local function call graph

#### Python control flow from main
- **Entry Point:** .github.scripts.changelog.create_review.main
- **Ordered Static Flow:**
  1. `.github.scripts.changelog.create_review.main`
  2. `.github.scripts.changelog.create_review.find_changelog_comment`
- **Evidence:** Static AST self/local function call graph

#### JavaScript/TypeScript entry flow: Node package main
- **Entry Point:** dist/index.cjs
- **Ordered Static Flow:**
  1. `dist/index.cjs`
  2. `Application modules/components`
- **Evidence:** backoffice-commons/package.json

#### JavaScript/TypeScript entry flow: Node package module
- **Entry Point:** dist/index.js
- **Ordered Static Flow:**
  1. `dist/index.js`
  2. `Application modules/components`
- **Evidence:** backoffice-commons/package.json

## 7. Dependencies and Compatibility

Dependencies are grouped by scope. Example/test/documentation dependencies do not contaminate the core technology stack.

### Development Dependencies

| Dependency | Current Version / Constraint | Source | Latest Version | Compatibility | Notes |
| --- | --- | --- | --- | --- | --- |
| @eslint/js | ^9.36.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @iconify/react | ^6.0.2 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @testing-library/jest-dom | ^6.8.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @testing-library/react | ^16.3.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @testing-library/user-event | ^14.6.1 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @types/luxon | ^3.7.1 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @types/node | ^24.5.2 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @types/react | ^19.1.13 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @types/react-dom | ^19.1.9 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @typescript-eslint/parser | ^8.44.1 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @vitejs/plugin-react | ^5.0.3 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| @vitest/ui | ^3.2.4 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| babel-eslint | ^10.1.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| del | ^8.0.1 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| eslint | ^9.36.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| eslint-config-prettier | ^10.1.8 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| eslint-plugin-import | ^2.32.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| eslint-plugin-prettier | ^5.5.4 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| eslint-plugin-react | ^7.37.5 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| eslint-plugin-react-hooks | ^5.2.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| eslint-plugin-react-refresh | ^0.4.21 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| globals | ^16.4.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| gulp | ^5.0.1 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| gulp-bump | ^3.2.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| gulp-eslint-new | ^2.5.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| jsdoc | ^4.0.4 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| jsdom | ^27.0.0 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| prettier | 3.6.2 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| rollup-plugin-visualizer | ^6.0.3 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| typescript | ~5.9.2 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| typescript-eslint | ^8.44.1 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| vite | ^7.1.7 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| vite-plugin-dts | ^4.5.4 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| vite-plugin-lib-inject-css | ^2.2.2 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |
| vitest | ^3.2.4 | backoffice-commons/package.json | Not available | Not checked - non-core dependency | Not available |

### Peer Dependencies

| Dependency | Current Version / Constraint | Source | Latest Version | Compatibility | Notes |
| --- | --- | --- | --- | --- | --- |
| @tanstack/react-table | ^8.21.3 | backoffice-commons/package.json | 9.2.4 | UNKNOWN | Latest version source: https://www.npmjs.com/package/@tanstack/react-table |
| bootstrap | ^5.3.6 | backoffice-commons/package.json | 5.3.8 | UNKNOWN | Latest version source: https://www.npmjs.com/package/bootstrap |
| debug | ^4.4.1 | backoffice-commons/package.json | 4.4.3 | UNKNOWN | Latest version source: https://www.npmjs.com/package/debug |
| luxon | ^3.6.1 | backoffice-commons/package.json | 3.7.2 | UNKNOWN | Latest version source: https://www.npmjs.com/package/luxon |
| react | ^19.1.0 | backoffice-commons/package.json | 19.3.0 | UNKNOWN | Latest version source: https://www.npmjs.com/package/react |
| react-bootstrap | ^2.10.10 | backoffice-commons/package.json | 2.10.10 | UNKNOWN | Latest version source: https://www.npmjs.com/package/react-bootstrap |
| react-router | ^7.6.2 | backoffice-commons/package.json | 8.4.0 | UNKNOWN | Latest version source: https://www.npmjs.com/package/react-router |
| react-toastify | ^11.0.5 | backoffice-commons/package.json | 11.1.0 | UNKNOWN | Latest version source: https://www.npmjs.com/package/react-toastify |

## 8. Tests and Coverage

- **Testing frameworks:** Jest
- **Test files detected:** 145
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
| bernacop | requests | Not available | POST | .github/scripts/bernacop/bernacop.py | Detected requests.post |
| bernacop | requests | Not available | GET | .github/scripts/bernacop/bernacop.py | Detected requests.get |
| bernacop | requests | Not available | PATCH | .github/scripts/bernacop/bernacop.py | Detected requests.patch |
| bernacop | requests | Not available | DELETE | .github/scripts/bernacop/bernacop.py | Detected requests.delete |
| embeddings | requests | https://api.openai.com/v1/embeddings | POST | .github/scripts/bernabot/knowledge/embeddings.py | Detected requests.post |
| diff_learner | requests | Not available | GET | .github/scripts/bernabot/knowledge/diff_learner.py | Detected requests.get |

## 11. Main Use Cases

No high-level use cases were returned by the local LLM.

## 12. Analysis Limitations

- Local LLM skipped; deterministic architecture and detailed static code flow are still reported.
