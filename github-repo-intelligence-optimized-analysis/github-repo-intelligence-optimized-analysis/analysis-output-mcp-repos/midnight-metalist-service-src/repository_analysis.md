# Repository Intelligent Analysis Report

## 1. Repository Summary

- **Repository:** midnight-metalist-service-src
- **Source:** https://github.com/NBCUDTC/midnight-metalist-service-src.git
- **Source Type:** GitHub
- **Repository Type:** Application / Service Repository
- **Files Analyzed:** 155
- **Local LLM Status:** Skipped by command line

### What the Application / Repository Does

Metalist is a service to store a set of configurations for a player to pull during playback. This is one of the services powering the overall system of live actions. Creates a timeline event in the database. Each request is additive and should contain a single moment. Update/overwrite previously published events. Gets the timeline events from the database for a specific pvid. Deletes a timeline event from the database. Gets health-check status. Returns 200 if all status checks are OK. Gets application metrics data. To be used for reporting prometheus metrics. Personalized Ad Service API uses Swag for documentation generation. To update API docs: 1. Add comments to your API handler in the Declarative Comments Format. 3. Run the following command in the project's root directory to generate the latest documentation: Remember to push the latest documentation generated under swagger directory to GitHub. 4. Once the app is started, Swagger UI is available at http://localhost:8081/swagger/index.html -   checkgofmt.sh a script run by pipeline-test.yaml that will fail if go source files aren't gofmt formatted

### Repository Summary

Metalist is a service to store a set of configurations for a player to pull during playback. This is one of the services powering the overall system of live actions. Creates a timeline event in the database. Each request is additive and should contain a single moment. Update/overwrite previously published events. Gets the timeline events from the database for a specific pvid. Deletes a timeline event from the database. Gets health-check status. Returns 200 if all status checks are OK. Gets application metrics data. To be used for reporting prometheus metrics. Personalized Ad Service API uses Swag for documentation generation. To update API docs: 1. Add comments to your API handler in the Declarative Comments Format. 3. Run the following command in the project's root directory to generate the latest documentation: Remember to push the latest documentation generated under swagger directory to GitHub. 4. Once the app is started, Swagger UI is available at http://localhost:8081/swagger/index.html -   checkgofmt.sh a script run by pipeline-test.yaml that will fail if go source files aren't gofmt formatted

## 2. Technology Stack

- **Languages:** Go, Shell
- **Frameworks:** Gin
- **Runtime:** Go 1.23.0
- **Databases:** MongoDB
- **Cloud Platforms:** Not detected
- **Containers:** Docker
- **Kubernetes Helm Terraform:** Helm
- **Ci Cd:** Not detected
- **Testing Tools:** Testify
- **Monitoring Observability:** Prometheus
- **Important Core Libraries:** github.com/beorn7/perks, github.com/bytedance/sonic, github.com/bytedance/sonic/loader, github.com/cespare/xxhash/v2, github.com/cloudwego/base64x, github.com/davecgh/go-spew, github.com/fsnotify/fsnotify, github.com/gabriel-vasile/mimetype, github.com/gin-contrib/graceful, github.com/gin-contrib/pprof, github.com/gin-contrib/sse, github.com/gin-gonic/gin, github.com/go-openapi/jsonpointer, github.com/go-openapi/jsonreference, github.com/go-openapi/spec, github.com/go-openapi/swag, github.com/go-playground/locales, github.com/go-playground/universal-translator, github.com/go-playground/validator/v10, github.com/go-viper/mapstructure/v2, github.com/goccy/go-json, github.com/golang/mock, github.com/golang/snappy, github.com/josharian/intern, github.com/json-iterator/go, github.com/klauspost/compress, github.com/klauspost/cpuid/v2, github.com/kylebanks/depth, github.com/leodido/go-urn, github.com/mailru/easyjson, github.com/mattn/go-isatty, github.com/modern-go/concurrent, github.com/modern-go/reflect2, github.com/montanaflynn/stats, github.com/munnerz/goautoneg, github.com/nbcudtc/midnight-go-tooling, github.com/pelletier/go-toml/v2, github.com/pmezard/go-difflib, github.com/prometheus/client-golang, github.com/prometheus/client-model, github.com/prometheus/common, github.com/prometheus/procfs, github.com/sagikazarmark/locafero, github.com/sourcegraph/conc, github.com/spf13/afero, github.com/spf13/cast, github.com/spf13/pflag, github.com/spf13/viper, github.com/stretchr/testify, github.com/subosito/gotenv, github.com/swaggo/files, github.com/swaggo/gin-swagger, github.com/swaggo/swag, github.com/twitchyliquid64/golang-asm, github.com/ugorji/go/codec, github.com/xdg-go/pbkdf2, github.com/xdg-go/scram, github.com/xdg-go/stringprep, github.com/youmark/pkcs8, go.mongodb.org/mongo-driver, go.uber.org/multierr, go.uber.org/zap, golang.org/x/arch, golang.org/x/crypto, golang.org/x/net, golang.org/x/sync, golang.org/x/sys, golang.org/x/text, golang.org/x/tools, google.golang.org/protobuf, gopkg.in/yaml.v3

## 3. Repository Scan and Engineering Artifacts

- **Important files:** Dockerfile, README.md, go.mod

- **Configuration:** cmd/app/config/config.yaml, tilt/deployments/mongo/config.yaml
- **Docker:** Dockerfile
- **Kubernetes Helm:** chart/Chart.yaml
- **Terraform:** Not detected
- **Ci Cd:** Not detected
- **Api Specs:** swagger/swagger.json
- **Documentation:** README.md, chart/README.md

## 4. Main Components and Code Structure

### internal
Internal implementation packages
**Evidence:** 111 analyzed core files under internal/

### chart
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 16 analyzed core files under chart/

### tilt
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 7 analyzed core files under tilt/

### cmd
Executable command entry points
**Evidence:** 5 analyzed core files under cmd/

### ci
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 4 analyzed core files under ci/

### swagger
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 2 analyzed core files under swagger/

### .github
Top-level source/component area; semantic responsibility refined by local LLM
**Evidence:** 1 analyzed core files under .github/

## 5. Code Architecture

- **Architecture Style:** Modular service / CLI architecture with executable entry points and reusable packages
- **Architecture Explanation:** The repository follows a modular service / cli architecture with executable entry points and reusable packages. Static analysis identified 7 major structural component areas, 1 executable/package entry points, and 35 repository-local dependency relationships. The architecture below is generated from source layout, imports, symbols, package metadata and executable entry points; the local LLM is used only to explain these facts in repository-specific language.

### Layers / Modules

| Layer / Module | Description | Evidence |
| --- | --- | --- |
| internal | Internal implementation packages | 111 analyzed core files under internal/ |
| chart | Top-level source/component area; semantic responsibility refined by local LLM | 16 analyzed core files under chart/ |
| tilt | Top-level source/component area; semantic responsibility refined by local LLM | 7 analyzed core files under tilt/ |
| cmd | Executable command entry points | 5 analyzed core files under cmd/ |
| ci | Top-level source/component area; semantic responsibility refined by local LLM | 4 analyzed core files under ci/ |
| swagger | Top-level source/component area; semantic responsibility refined by local LLM | 2 analyzed core files under swagger/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 1 analyzed core files under .github/ |

### Entry Points

| Type | Symbol / Command | Source File |
| --- | --- | --- |
| Go executable entry point | cmd:main | cmd/main.go |

### Major Components

| Component | Responsibility | Evidence |
| --- | --- | --- |
| internal | Internal implementation packages | 111 analyzed core files under internal/ |
| chart | Top-level source/component area; semantic responsibility refined by local LLM | 16 analyzed core files under chart/ |
| tilt | Top-level source/component area; semantic responsibility refined by local LLM | 7 analyzed core files under tilt/ |
| cmd | Executable command entry points | 5 analyzed core files under cmd/ |
| ci | Top-level source/component area; semantic responsibility refined by local LLM | 4 analyzed core files under ci/ |
| swagger | Top-level source/component area; semantic responsibility refined by local LLM | 2 analyzed core files under swagger/ |
| .github | Top-level source/component area; semantic responsibility refined by local LLM | 1 analyzed core files under .github/ |

### Component Relationships

| From | To | Relationship |
| --- | --- | --- |
| cmd | cmd/app | imports/depends on |
| internal/handler | internal/lib/docs | imports/depends on |
| internal/handler | internal/lib/router | imports/depends on |
| internal/handler | internal/lib/router/pipeline | imports/depends on |
| internal/handler | internal/view | imports/depends on |
| internal/handler | internal/lib/metrics | imports/depends on |
| internal/handler | internal/lib/constant | imports/depends on |
| internal/handler | internal/lib/etag | imports/depends on |
| internal/handler | internal/lib/router/response | imports/depends on |
| internal/handler | internal/lib/utils | imports/depends on |
| internal/repository | internal/entity | imports/depends on |
| internal/repository | internal/lib/search | imports/depends on |
| internal/repository | internal/domain | imports/depends on |
| internal/server | internal/handler | imports/depends on |
| internal/server | internal/lib/metrics | imports/depends on |
| internal/dal | internal/domain | imports/depends on |
| internal/dal | internal/entity | imports/depends on |
| internal/dal | internal/lib/search | imports/depends on |
| internal/usecase | internal/domain | imports/depends on |
| internal/usecase | internal/lib/search | imports/depends on |
| internal/usecase | internal/view | imports/depends on |
| internal/usecase | internal/lib/constant | imports/depends on |
| internal/domain | internal/lib/search | imports/depends on |
| internal/lib/metrics | internal/domain | imports/depends on |
| internal/lib/router/pipeline | internal/lib/router | imports/depends on |
| internal/lib/router/pipeline | internal/lib/metrics | imports/depends on |
| internal/lib/router/pipeline | internal/lib/etag | imports/depends on |
| cmd/app | internal/domain | imports/depends on |
| cmd/app | internal/dal | imports/depends on |
| cmd/app | internal/handler | imports/depends on |
| cmd/app | internal/lib/metrics | imports/depends on |
| cmd/app | internal/repository | imports/depends on |
| cmd/app | internal/server | imports/depends on |
| cmd/app | internal/service | imports/depends on |
| cmd/app | internal/usecase | imports/depends on |

### Configuration Model

Repository contains explicit configuration artifacts: cmd/app/config/config.yaml, tilt/deployments/mongo/config.yaml.

### Extension Points

No explicit extension points were statically identified.

### Deployment Model

Docker, Kubernetes/Helm

### Architecture Data / Control Flow

1. Execution begins at the detected repository entry point(s): cmd/main.go.
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

#### Step 1: Start the application

Execution starts in cmd/main.go at main. The startup function then delegates into the application bootstrap code shown below.

**Code / files involved:**
- `cmd/main.go:main`
- `app.Run`

**What happens next:** Control moves into application initialization.

**Evidence:** cmd/main.go

#### Step 2: Load runtime configuration

The application uses the detected configuration files during startup. Configuration values control later runtime initialization; values not proven from source are not guessed.

**Code / files involved:**
- `cmd/app/config/config.yaml`
- `tilt/deployments/mongo/config.yaml`

**What happens next:** Validated runtime settings are available to the bootstrap code.

**Evidence:** cmd/app/config/config.yaml, tilt/deployments/mongo/config.yaml

#### Step 3: Build application dependencies and start the server

The main bootstrap creates the runtime dependencies in code order. The detected calls include logging/metrics setup, database/client connection, repository/use-case/handler construction, HTTP server creation and service start where present.

**Code / files involved:**
- `cmd/app/app.go:Run`
- `fmt.Printf`
- `os.Exit`
- `err.Error`
- `logger.NewLogger`
- `metrics.RegisterMetrics`
- `metrics.NewTracker`
- `dal.ConnectDB`
- `repository.NewGlobalConfigsRepo`
- `dal.NewGlobalConfigsDAL`
- `dbClient.Database`
- `repository.NewTimelineEventRepo`
- `dal.NewTimelineEventDAL`
- `repository.NewTimelineEventArchiveRepo`
- `dal.NewTimelineEventArchiveDAL`
- `repository.NewRawLinearEventRepo`
- `dal.NewRawLinearEventDAL`
- `usecase.NewMetalistService`
- `usecase.NewStatsService`
- `usecase.NewRawLinearEventService`
- `handler.NewMetalistHandler`
- `handler.NewStatsHandler`
- `metrics.NewHandler`

**What happens next:** The service is initialized and ready to receive runtime work.

**Evidence:** cmd/app/app.go

### GetTimelineEvents Flow

#### Step 4: Process GET /metalist/api/v1/:pvid

A GET request to `/metalist/api/v1/:pvid` is routed to `GetTimelineEvents`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `client.FindOne`, `result.Decode`, `options.Find`, `client.Find`, `cursor.Decode`.

**Code / files involved:**
- `GET /metalist/api/v1/:pvid`
- `internal/handler/metalist.go:MetalistHandler.GetTimelineEvents`
- `internal/usecase/metalist.go:MetalistService.GetTimelineEvents`
- `internal/usecase/metalist.go:MetalistService.parseEventDataByTypeToView`
- `internal/repository/globalConfigs.go:GlobalConfigsRepo.GetGlobalConfigs`
- `internal/dal/globalConfigs.go:GlobalConfigsDAL.FindOne`
- `internal/repository/timelineEvent.go:TimelineEventRepo.GetTimelineEvents`
- `internal/dal/timelineEvent.go:TimelineEventDAL.FindAllByParams`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go, internal/usecase/metalist.go, internal/repository/globalConfigs.go, internal/dal/globalConfigs.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go

### GetPredefinedTimelineEvents Flow

#### Step 5: Process GET /metalist/api/v1/temporary/:pvid

A GET request to `/metalist/api/v1/temporary/:pvid` is routed to `GetPredefinedTimelineEvents`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing.

**Code / files involved:**
- `GET /metalist/api/v1/temporary/:pvid`
- `internal/handler/metalist.go:MetalistHandler.GetPredefinedTimelineEvents`
- `internal/usecase/metalist.go:MetalistService.GetPredefinedTimelineEvents`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go

### CreateTimelineEvent Flow

#### Step 6: Process POST /metalist/api/v1/:pvid

A POST request to `/metalist/api/v1/:pvid` is routed to `CreateTimelineEvent`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `client.CountDocuments`, `client.InsertOne`.

**Code / files involved:**
- `POST /metalist/api/v1/:pvid`
- `internal/handler/metalist.go:MetalistHandler.CreateTimelineEvent`
- `internal/usecase/metalist.go:MetalistService.CreateTimelineEvent`
- `internal/usecase/metalist.go:MetalistService.parseEventDataByTypeToDomain`
- `internal/repository/timelineEvent.go:TimelineEventRepo.GetDocumentCountByParams`
- `internal/dal/timelineEvent.go:TimelineEventDAL.GetDocumentCountByParams`
- `internal/repository/timelineEvent.go:TimelineEventRepo.CreateTimelineEvent`
- `internal/dal/timelineEvent.go:TimelineEventDAL.InsertOne`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go, internal/usecase/metalist.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go

### UpdateTimelineEvent Flow

#### Step 7: Process PATCH /metalist/api/v1/:pvid/:eventid

A PATCH request to `/metalist/api/v1/:pvid/:eventid` is routed to `UpdateTimelineEvent`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `options.Find`, `client.Find`, `cursor.Decode`, `client.UpdateOne`.

**Code / files involved:**
- `PATCH /metalist/api/v1/:pvid/:eventid`
- `internal/handler/metalist.go:MetalistHandler.UpdateTimelineEvent`
- `internal/usecase/metalist.go:MetalistService.UpdateTimelineEvent`
- `internal/usecase/metalist.go:MetalistService.validateEventTimes`
- `internal/usecase/metalist.go:MetalistService.parseUpdateEventData`
- `internal/repository/timelineEvent.go:TimelineEventRepo.GetTimelineEvents`
- `internal/dal/timelineEvent.go:TimelineEventDAL.FindAllByParams`
- `internal/repository/timelineEvent.go:TimelineEventRepo.UpdateTimelineEvent`
- `internal/dal/timelineEvent.go:TimelineEventDAL.UpdateOneByParams`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go, internal/usecase/metalist.go, internal/usecase/metalist.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go

### DeleteTimelineEvent Flow

#### Step 8: Process DELETE /metalist/api/v1/:pvid/:eventid

A DELETE request to `/metalist/api/v1/:pvid/:eventid` is routed to `DeleteTimelineEvent`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `options.Find`, `client.Find`, `cursor.Decode`, `client.DeleteOne`.

**Code / files involved:**
- `DELETE /metalist/api/v1/:pvid/:eventid`
- `internal/handler/metalist.go:MetalistHandler.DeleteTimelineEvent`
- `internal/usecase/metalist.go:MetalistService.DeleteTimelineEvent`
- `internal/repository/timelineEvent.go:TimelineEventRepo.GetTimelineEvents`
- `internal/dal/timelineEvent.go:TimelineEventDAL.FindAllByParams`
- `internal/repository/timelineEvent.go:TimelineEventRepo.DeleteTimelineEvent`
- `internal/dal/timelineEvent.go:TimelineEventDAL.DeleteOneByParams`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go

### ArchiveTimelineEventsByType Flow

#### Step 9: Process POST /metalist/api/v1/archive/:type

A POST request to `/metalist/api/v1/archive/:type` is routed to `ArchiveTimelineEventsByType`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `options.Find`, `client.Find`, `cursor.Decode`, `options.BulkWrite`, `client.BulkWrite`.

**Code / files involved:**
- `POST /metalist/api/v1/archive/:type`
- `internal/handler/metalist.go:MetalistHandler.ArchiveTimelineEventsByType`
- `internal/usecase/metalist.go:MetalistService.ArchiveTimelineEventsByType`
- `internal/usecase/metalist.go:MetalistService.performArchiveTimelineEvents`
- `internal/repository/timelineEvent.go:TimelineEventRepo.GetTimelineEvents`
- `internal/dal/timelineEvent.go:TimelineEventDAL.FindAllByParams`
- `internal/repository/timelineEventArchive.go:TimelineEventArchiveRepo.CreateTimelineEventArchives`
- `internal/dal/timelineEventArchive.go:TimelineEventArchiveDAL.BulkInsert`
- `internal/repository/timelineEvent.go:TimelineEventRepo.DeleteTimelineEvents`
- `internal/dal/timelineEvent.go:TimelineEventDAL.BulkDelete`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go, internal/usecase/metalist.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go, internal/repository/timelineEventArchive.go, internal/dal/timelineEventArchive.go, internal/repository/timelineEvent.go

### Archives Timeline Events Flow

#### Step 10: Process POST /metalist/api/v1/archive

A POST request to `/metalist/api/v1/archive` is routed to `ArchiveTimelineEvents`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `options.Find`, `client.Find`, `cursor.Decode`, `options.BulkWrite`, `client.BulkWrite`.

**Code / files involved:**
- `POST /metalist/api/v1/archive`
- `internal/handler/metalist.go:MetalistHandler.ArchiveTimelineEvents`
- `internal/usecase/metalist.go:MetalistService.ArchiveTimelineEvents`
- `internal/usecase/metalist.go:MetalistService.performArchiveTimelineEvents`
- `internal/repository/timelineEvent.go:TimelineEventRepo.GetTimelineEvents`
- `internal/dal/timelineEvent.go:TimelineEventDAL.FindAllByParams`
- `internal/repository/timelineEventArchive.go:TimelineEventArchiveRepo.CreateTimelineEventArchives`
- `internal/dal/timelineEventArchive.go:TimelineEventArchiveDAL.BulkInsert`
- `internal/repository/timelineEvent.go:TimelineEventRepo.DeleteTimelineEvents`
- `internal/dal/timelineEvent.go:TimelineEventDAL.BulkDelete`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go, internal/usecase/metalist.go, internal/repository/timelineEvent.go, internal/dal/timelineEvent.go, internal/repository/timelineEventArchive.go, internal/dal/timelineEventArchive.go, internal/repository/timelineEvent.go

### Gets Global Configs Flow

#### Step 11: Process GET /metalist/api/v1/configs

A GET request to `/metalist/api/v1/configs` is routed to `GetGlobalConfigs`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `client.FindOne`, `result.Decode`.

**Code / files involved:**
- `GET /metalist/api/v1/configs`
- `internal/handler/metalist.go:MetalistHandler.GetGlobalConfigs`
- `internal/usecase/metalist.go:MetalistService.GetGlobalConfigs`
- `internal/repository/globalConfigs.go:GlobalConfigsRepo.GetGlobalConfigs`
- `internal/dal/globalConfigs.go:GlobalConfigsDAL.FindOne`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go, internal/repository/globalConfigs.go, internal/dal/globalConfigs.go

### Updates Global Configs Flow

#### Step 12: Process PUT /metalist/api/v1/configs

A PUT request to `/metalist/api/v1/configs` is routed to `UpdateGlobalConfigs`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `client.UpdateOne`.

**Code / files involved:**
- `PUT /metalist/api/v1/configs`
- `internal/handler/metalist.go:MetalistHandler.UpdateGlobalConfigs`
- `internal/usecase/metalist.go:MetalistService.UpdateGlobalConfigs`
- `internal/repository/globalConfigs.go:GlobalConfigsRepo.UpdateGlobalConfigs`
- `internal/dal/globalConfigs.go:GlobalConfigsDAL.UpdateOne`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/metalist.go, internal/usecase/metalist.go, internal/repository/globalConfigs.go, internal/dal/globalConfigs.go

### Get System Health Flow

#### Step 13: Process GET /api/health

A GET request to `/api/health` is routed to `GetHealth`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing.

**Code / files involved:**
- `GET /api/health`
- `internal/handler/stats.go:StatsHandler.GetHealth`
- `internal/usecase/stats.go:StatsService.GetHealth`
- `internal/repository/timelineEvent.go:TimelineEventRepo.CheckDatabaseConnection`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/stats.go, internal/usecase/stats.go, internal/repository/timelineEvent.go

### Get Metadata Flow

#### Step 14: Process GET /api/meta

A GET request to `/api/meta` is routed to `GetMetaMetrics`. Production control then follows the proven handler/service/repository/data-access chain in the code list below.

**Code / files involved:**
- `GET /api/meta`
- `internal/handler/stats.go:StatsHandler.GetMetaMetrics`
- `internal/usecase/stats.go:StatsService.GetMetaMetrics`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/stats.go, internal/usecase/stats.go

### Get System Metrics Flow

#### Step 15: Process GET /api/metrics

A GET request to `/api/metrics` is routed to `GetMetrics`. Production control then follows the proven handler/service/repository/data-access chain in the code list below.

**Code / files involved:**
- `GET /api/metrics`
- `internal/handler/stats.go:StatsHandler.GetMetrics`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/stats.go

### Get Configuration Flow

#### Step 16: Process GET /private/config

A GET request to `/private/config` is routed to `GetConfiguration`. Production control then follows the proven handler/service/repository/data-access chain in the code list below.

**Code / files involved:**
- `GET /private/config`
- `internal/handler/stats.go:StatsHandler.GetConfiguration`
- `internal/usecase/stats.go:StatsService.GetConfiguration`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/stats.go, internal/usecase/stats.go

### ReturnEmpty Flow

#### Step 17: Process GET /swagger/*any

A GET request to `/swagger/*any` is routed to `ReturnEmpty`. Production control then follows the proven handler/service/repository/data-access chain in the code list below.

**Code / files involved:**
- `GET /swagger/*any`
- `internal/handler/docs.go:DocHandler.ReturnEmpty`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/docs.go

### GetRawLinearEvents Flow

#### Step 18: Process GET /api/v1/raw-linear-events/:region/:serviceKey

A GET request to `/api/v1/raw-linear-events/:region/:serviceKey` is routed to `GetRawLinearEvents`. Production control then follows the proven handler/service/repository/data-access chain in the code list below. The handler or business layer validates request/business conditions before continuing. The flow reaches the detected database operations: `client.CountDocuments`, `options.Find`, `client.Find`, `cursor.Decode`.

**Code / files involved:**
- `GET /api/v1/raw-linear-events/:region/:serviceKey`
- `internal/handler/rawLinearEvent.go:RawLinearEventHandler.GetRawLinearEvents`
- `internal/usecase/rawLinearEvent.go:RawLinearEventService.GetRawLinearEvents`
- `internal/repository/rawLinearEvent.go:RawLinearEventRepo.GetRawLinearEventsByLSKAndWindow`
- `internal/dal/rawLinearEvent.go:RawLinearEventDAL.FindByParams`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** internal/handler/handler.go, internal/handler/rawLinearEvent.go, internal/usecase/rawLinearEvent.go, internal/repository/rawLinearEvent.go, internal/dal/rawLinearEvent.go

### Gets Raw Linear Events Flow

#### Step 19: Process GET /api/v1/raw-linear-events/{region}/{serviceKey}

A GET request to `/api/v1/raw-linear-events/{region}/{serviceKey}` is routed to `the documented operation`.

**Code / files involved:**
- `GET /api/v1/raw-linear-events/{region}/{serviceKey}`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** swagger/swagger.json

### Archives Timeline Events Flow

#### Step 20: Process POST /metalist/api/v1/archive/{type}

A POST request to `/metalist/api/v1/archive/{type}` is routed to `the documented operation`.

**Code / files involved:**
- `POST /metalist/api/v1/archive/{type}`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** swagger/swagger.json

### Gets Timeline Events Flow

#### Step 21: Process GET /metalist/api/v1/{pvid}

A GET request to `/metalist/api/v1/{pvid}` is routed to `the documented operation`.

**Code / files involved:**
- `GET /metalist/api/v1/{pvid}`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** swagger/swagger.json

### Creates a Timeline Event Flow

#### Step 22: Process POST /metalist/api/v1/{pvid}

A POST request to `/metalist/api/v1/{pvid}` is routed to `the documented operation`.

**Code / files involved:**
- `POST /metalist/api/v1/{pvid}`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** swagger/swagger.json

### Deletes Timeline Event Flow

#### Step 23: Process DELETE /metalist/api/v1/{pvid}/{eventid}

A DELETE request to `/metalist/api/v1/{pvid}/{eventid}` is routed to `the documented operation`.

**Code / files involved:**
- `DELETE /metalist/api/v1/{pvid}/{eventid}`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** swagger/swagger.json

### Updates a Timeline Event Flow

#### Step 24: Process PATCH /metalist/api/v1/{pvid}/{eventid}

A PATCH request to `/metalist/api/v1/{pvid}/{eventid}` is routed to `the documented operation`.

**Code / files involved:**
- `PATCH /metalist/api/v1/{pvid}/{eventid}`

**What happens next:** The processed result returns through the application layers to the HTTP response path.

**Evidence:** swagger/swagger.json

### Application Shutdown Flow

#### Step 25: Gracefully stop the service

The application waits for the detected operating-system termination signals and invokes the graceful shutdown path so active work can finish before process exit.

**Code / files involved:**
- `internal/service/service.go:Service.Shutdown`
- `httpServer.Shutdown`

**What happens next:** The HTTP service shuts down and the application exits.

**Evidence:** internal/service/service.go

### Static Call / Module Paths

The paths below are the exact callable/import chains that static analysis could prove. They support the simplified flow above.

#### Go execution/package flow from cmd
- **Entry Point:** cmd/main.go
- **Ordered Static Flow:**
  1. `cmd`
  2. `cmd/app`
  3. `internal/domain`
  4. `internal/dal`
  5. `internal/handler`
  6. `internal/lib/metrics`
  7. `internal/lib/search`
  8. `internal/entity`
  9. `internal/lib/docs`
  10. `internal/lib/router`
  11. `internal/lib/router/pipeline`
  12. `internal/view`
- **Evidence:** Static Go package import graph

## 7. Dependencies and Compatibility

Dependencies are grouped by scope. Example/test/documentation dependencies do not contaminate the core technology stack.

### Core Dependencies

| Dependency | Current Version / Constraint | Source | Latest Version | Compatibility | Notes |
| --- | --- | --- | --- | --- | --- |
| github.com/beorn7/perks | v1.0.1 | go.mod | v1.0.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/beorn7/perks |
| github.com/bytedance/sonic | v1.13.1 | go.mod | v1.15.4 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/bytedance/sonic |
| github.com/bytedance/sonic/loader | v0.2.4 | go.mod | v0.5.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/bytedance/sonic/loader |
| github.com/cespare/xxhash/v2 | v2.3.0 | go.mod | v2.3.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/cespare/xxhash/v2 |
| github.com/cloudwego/base64x | v0.1.5 | go.mod | v0.1.7 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/cloudwego/base64x |
| github.com/davecgh/go-spew | v1.1.1 | go.mod | v1.1.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/davecgh/go-spew |
| github.com/fsnotify/fsnotify | v1.8.0 | go.mod | v1.10.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/fsnotify/fsnotify |
| github.com/gabriel-vasile/mimetype | v1.4.8 | go.mod | v1.4.15 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/gabriel-vasile/mimetype |
| github.com/gin-contrib/graceful | v1.1.1 | go.mod | v1.2.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/gin-contrib/graceful |
| github.com/gin-contrib/pprof | v1.5.2 | go.mod | v1.5.5 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/gin-contrib/pprof |
| github.com/gin-contrib/sse | v1.0.0 | go.mod | v1.1.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/gin-contrib/sse |
| github.com/gin-gonic/gin | v1.10.0 | go.mod | v1.12.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/gin-gonic/gin |
| github.com/go-openapi/jsonpointer | v0.21.1 | go.mod | v1.0.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/jsonpointer |
| github.com/go-openapi/jsonreference | v0.21.0 | go.mod | v1.0.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/jsonreference |
| github.com/go-openapi/spec | v0.21.0 | go.mod | v1.0.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/spec |
| github.com/go-openapi/swag | v0.23.1 | go.mod | v0.29.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-openapi/swag |
| github.com/go-playground/locales | v0.14.1 | go.mod | v0.14.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/go-playground/locales |
| github.com/go-playground/universal-translator | v0.18.1 | go.mod | v0.18.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/go-playground/universal-translator |
| github.com/go-playground/validator/v10 | v10.25.0 | go.mod | v10.30.4 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-playground/validator/v10 |
| github.com/go-viper/mapstructure/v2 | v2.2.1 | go.mod | v2.5.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/go-viper/mapstructure/v2 |
| github.com/goccy/go-json | v0.10.5 | go.mod | v0.10.6 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/goccy/go-json |
| github.com/golang/mock | v1.6.0 | go.mod | v1.6.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/golang/mock |
| github.com/golang/snappy | v1.0.0 | go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/golang/snappy |
| github.com/josharian/intern | v1.0.0 | go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/josharian/intern |
| github.com/json-iterator/go | v1.1.12 | go.mod | v1.1.12 | CURRENT | Latest version source: https://pkg.go.dev/github.com/json-iterator/go |
| github.com/klauspost/compress | v1.18.0 | go.mod | v1.20.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/klauspost/compress |
| github.com/klauspost/cpuid/v2 | v2.2.10 | go.mod | v2.4.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/klauspost/cpuid/v2 |
| github.com/KyleBanks/depth | v1.2.1 | go.mod | v1.2.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/KyleBanks/depth |
| github.com/leodido/go-urn | v1.4.0 | go.mod | v1.5.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/leodido/go-urn |
| github.com/mailru/easyjson | v0.9.0 | go.mod | v0.9.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/mailru/easyjson |
| github.com/mattn/go-isatty | v0.0.20 | go.mod | v0.0.24 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/mattn/go-isatty |
| github.com/modern-go/concurrent | v0.0.0-20180306012644-bacd9c7ef1dd | go.mod | v0.0.0-20180306012644-bacd9c7ef1dd | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/modern-go/concurrent |
| github.com/modern-go/reflect2 | v1.0.2 | go.mod | v1.0.2 | CURRENT | Latest version source: https://pkg.go.dev/github.com/modern-go/reflect2 |
| github.com/montanaflynn/stats | v0.7.1 | go.mod | v0.12.6 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/montanaflynn/stats |
| github.com/munnerz/goautoneg | v0.0.0-20191010083416-a7dc8b61c822 | go.mod | v0.0.0-20191010083416-a7dc8b61c822 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/munnerz/goautoneg |
| github.com/NBCUDTC/midnight-go-tooling | v1.1.32 | go.mod | Not available | UNKNOWN | Latest version source: go.mod |
| github.com/pelletier/go-toml/v2 | v2.2.3 | go.mod | v2.4.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/pelletier/go-toml/v2 |
| github.com/pmezard/go-difflib | v1.0.0 | go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/pmezard/go-difflib |
| github.com/prometheus/client_golang | v1.21.1 | go.mod | v1.24.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/client_golang |
| github.com/prometheus/client_model | v0.6.1 | go.mod | v0.6.3 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/client_model |
| github.com/prometheus/common | v0.63.0 | go.mod | v0.71.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/common |
| github.com/prometheus/procfs | v0.16.0 | go.mod | v0.22.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/prometheus/procfs |
| github.com/sagikazarmark/locafero | v0.8.0 | go.mod | v0.12.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/sagikazarmark/locafero |
| github.com/sourcegraph/conc | v0.3.0 | go.mod | v0.3.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/sourcegraph/conc |
| github.com/spf13/afero | v1.14.0 | go.mod | v1.15.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/spf13/afero |
| github.com/spf13/cast | v1.7.1 | go.mod | v1.10.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/spf13/cast |
| github.com/spf13/pflag | v1.0.6 | go.mod | v1.0.10 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/spf13/pflag |
| github.com/spf13/viper | v1.20.0 | go.mod | v1.21.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/spf13/viper |
| github.com/stretchr/testify | v1.10.0 | go.mod | v1.12.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/stretchr/testify |
| github.com/subosito/gotenv | v1.6.0 | go.mod | v1.6.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/subosito/gotenv |
| github.com/swaggo/files | v1.0.1 | go.mod | v1.0.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/swaggo/files |
| github.com/swaggo/gin-swagger | v1.6.0 | go.mod | v1.6.1 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/swaggo/gin-swagger |
| github.com/swaggo/swag | v1.16.4 | go.mod | v1.16.6 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/swaggo/swag |
| github.com/twitchyliquid64/golang-asm | v0.15.1 | go.mod | v0.15.1 | CURRENT | Latest version source: https://pkg.go.dev/github.com/twitchyliquid64/golang-asm |
| github.com/ugorji/go/codec | v1.2.12 | go.mod | v1.3.2 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/ugorji/go/codec |
| github.com/xdg-go/pbkdf2 | v1.0.0 | go.mod | v1.0.0 | CURRENT | Latest version source: https://pkg.go.dev/github.com/xdg-go/pbkdf2 |
| github.com/xdg-go/scram | v1.1.2 | go.mod | v1.2.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/github.com/xdg-go/scram |
| github.com/xdg-go/stringprep | v1.0.4 | go.mod | v1.0.4 | CURRENT | Latest version source: https://pkg.go.dev/github.com/xdg-go/stringprep |
| github.com/youmark/pkcs8 | v0.0.0-20240726163527-a2c0da244d78 | go.mod | v0.0.0-20240726163527-a2c0da244d78 | UNKNOWN | Latest version source: https://pkg.go.dev/github.com/youmark/pkcs8 |
| go.mongodb.org/mongo-driver | v1.17.3 | go.mod | v1.17.10 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.mongodb.org/mongo-driver |
| go.uber.org/multierr | v1.11.0 | go.mod | v1.11.0 | CURRENT | Latest version source: https://pkg.go.dev/go.uber.org/multierr |
| go.uber.org/zap | v1.27.0 | go.mod | v1.28.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/go.uber.org/zap |
| golang.org/x/arch | v0.15.0 | go.mod | v0.31.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/arch |
| golang.org/x/crypto | v0.36.0 | go.mod | v0.57.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/crypto |
| golang.org/x/net | v0.37.0 | go.mod | v0.59.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/net |
| golang.org/x/sync | v0.12.0 | go.mod | v0.23.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/sync |
| golang.org/x/sys | v0.31.0 | go.mod | v0.48.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/sys |
| golang.org/x/text | v0.23.0 | go.mod | v0.42.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/text |
| golang.org/x/tools | v0.31.0 | go.mod | v0.50.0 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/golang.org/x/tools |
| google.golang.org/protobuf | v1.36.5 | go.mod | v1.36.12 | UPDATE_AVAILABLE | A newer stable version is available. Review the authoritative package source and official release notes before upgrading. \| Latest version source: https://pkg.go.dev/google.golang.org/protobuf |
| gopkg.in/yaml.v3 | v3.0.1 | go.mod | v3.0.1 | CURRENT | Latest version source: https://pkg.go.dev/gopkg.in/yaml.v3 |

## 8. Tests and Coverage

- **Testing frameworks:** Testify
- **Test files detected:** 35
- **Coverage status:** Actual coverage result not found
- **Coverage percentage:** Not available
- **Coverage source:** Not available

## 9. Production Internal APIs

_Test/mock/example routes are excluded._

| Method | Endpoint | Handler | Component | Source File |
| --- | --- | --- | --- | --- |
| GET | /metalist/api/v1/:pvid | GetTimelineEvents | HTTP route | internal/handler/handler.go |
| GET | /metalist/api/v1/temporary/:pvid | GetPredefinedTimelineEvents | HTTP route | internal/handler/handler.go |
| POST | /metalist/api/v1/:pvid | CreateTimelineEvent | HTTP route | internal/handler/handler.go |
| PATCH | /metalist/api/v1/:pvid/:eventid | UpdateTimelineEvent | HTTP route | internal/handler/handler.go |
| DELETE | /metalist/api/v1/:pvid/:eventid | DeleteTimelineEvent | HTTP route | internal/handler/handler.go |
| POST | /metalist/api/v1/archive/:type | ArchiveTimelineEventsByType | HTTP route | internal/handler/handler.go |
| POST | /metalist/api/v1/archive | ArchiveTimelineEvents | HTTP route | internal/handler/handler.go |
| GET | /metalist/api/v1/configs | GetGlobalConfigs | HTTP route | internal/handler/handler.go |
| PUT | /metalist/api/v1/configs | UpdateGlobalConfigs | HTTP route | internal/handler/handler.go |
| GET | /api/health | GetHealth | HTTP route | internal/handler/handler.go |
| GET | /api/meta | GetMetaMetrics | HTTP route | internal/handler/handler.go |
| GET | /api/metrics | GetMetrics | HTTP route | internal/handler/handler.go |
| GET | /private/config | GetConfiguration | HTTP route | internal/handler/handler.go |
| GET | /swagger/*any | ReturnEmpty | HTTP route | internal/handler/handler.go |
| GET | /api/v1/raw-linear-events/:region/:serviceKey | GetRawLinearEvents | HTTP route | internal/handler/handler.go |
| GET | /api/v1/raw-linear-events/{region}/{serviceKey} | Not available | HTTP route | swagger/swagger.json |
| POST | /metalist/api/v1/archive/{type} | Not available | HTTP route | swagger/swagger.json |
| GET | /metalist/api/v1/{pvid} | Not available | HTTP route | swagger/swagger.json |
| POST | /metalist/api/v1/{pvid} | Not available | HTTP route | swagger/swagger.json |
| DELETE | /metalist/api/v1/{pvid}/{eventid} | Not available | HTTP route | swagger/swagger.json |
| PATCH | /metalist/api/v1/{pvid}/{eventid} | Not available | HTTP route | swagger/swagger.json |

## 10. Production External API and Integration Calls

_Test/mock/example calls are excluded._

_Not detected._

## 11. Main Use Cases

No high-level use cases were returned by the local LLM.

## 12. Analysis Limitations

- Local LLM skipped; deterministic architecture and detailed static code flow are still reported.
