**I build backend systems, infrastructure, and AI products - with concurrency, observability, and recovery designed in.**

My work connects three things: useful products, explicit system guarantees, and evidence that the implementation holds up. Today, that means production AI agents and contributions to the tools those systems depend on.

[LinkedIn](https://www.linkedin.com/in/ghdtjdwn/) · [Email](mailto:seongjuice999@gmail.com) · [한국어](./README_KR.md)

## Experience

- [Bizarre Cube AI](https://www.bzrr.ai/) / [MXN Commerce Group](https://www.mxncommerce.com/en) Software Engineer Intern (2026.09 ~ ) · [Organization](https://github.com/bizarrecube)
- [JECT](https://ject.kr/) Backend & Infrastructure Engineer (2026.09 ~ ) · [Backend](https://github.com/JECT-Study/Billit-5th-Server) · [Infrastructure](https://github.com/JECT-Study/Billit-5th-Infra)
- [TrabyOS](https://github.com/TrabyOS) Co-founder & CTO (2026.07 ~ 2026.10)
- Soongsil University Computer Science (2022.03 ~ ) · [Coursework across 12 subjects](https://github.com/ghdtjdwn/cs-coursework)
- Republic of Korea Army Military Service (2023.05 ~ 2024.11)

## Open source

**7 changes accepted across 6 upstream repositories** - six directly merged PRs and one change cherry-picked by a maintainer. My focus is observability, cancellation, state consistency, and regression tests. Status checked **2026-10-19**.

### [OpenTelemetry](https://github.com/open-telemetry) · From one instrumentation bug to shared test infrastructure

- **Turn a PR-local test into a maintainer-requested shared utility.** An OpenTelemetry maintainer [asked for one shared sampler in the core test utilities](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5073#discussion_r4061037725) instead of a copy in each instrumentation, and [pointed my WSGI fix to that request](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032#discussion_r4061074604). I implemented `CapturingSampler`, released in **1.45.0** and now reused in the tests of **8 HTTP instrumentation packages**: WSGI, Django, ASGI, aiohttp-server, Falcon, Flask, Pyramid, and Tornado. [Core #5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681) · [Adoption example](https://github.com/open-telemetry/opentelemetry-python-contrib/blob/de43f819a4a919213d246a23e62a1b256aeca7b9/instrumentation/opentelemetry-instrumentation-asgi/tests/test_asgi_custom_headers.py)
- **Make headers available when sampling happens.** Fixed WSGI request-header collection at span creation, with sanitized values kept out of internal spans and metrics. Merged with approvals from three maintainers. [Contrib #5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032)
- **Follow the change into the rest of the ecosystem.** Verified and reviewed **6 follow-up instrumentation PRs**. Found Tornado ignoring sensitive-header masking settings and fixed it using the shared capture helper. [Contrib #5170](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5170) · [Tracking issue #4975](https://github.com/open-telemetry/opentelemetry-python-contrib/issues/4975)

### Reliability work beyond my own applications

- **[Ouroboros #2365](https://github.com/Q00/ouroboros/pull/2365) · Cancellation cleanup - merged, v0.54.5.** Fixed leaked HTTP resources and stale connected state when MCP initialization is cancelled; added **6 regression tests**.
- **[psycopg #1345](https://github.com/psycopg/psycopg/issues/1345) · Async pool cancellation - reproduction & verification.** Reproduced swallowed cancellation, supplied a deterministic regression test, and verified the maintainer's fix, released in psycopg_pool 3.3.2. This contribution is separate from the 7 accepted changes above.
- **[Micrometer #7925](https://github.com/micrometer-metrics/micrometer/pull/7925) · Tested observability documentation - merged.** Documented custom Java HttpClient observation tags with examples compiled and exercised by the test suite.
- **[Ponytail #828](https://github.com/DietrichGebert/ponytail/pull/828) · Branch-specific state restoration - merged, v4.13.0.** Restored the selected branch's saved mode after conversation-tree navigation.
- **[Caveman #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · Reliable forced updates - adopted in v2.7.0.** Repaired rule-file updates for **3 editors** with regression tests. The maintainer cherry-picked the change into [#1015](https://github.com/JuliusBrussee/caveman/pull/1015).

## Awards

- 🏆 **Manifest Special Award** · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 **Silver Prize** · Soongsil University CS Software Competition 2026 · [Cham Domi](https://github.com/chamdormie)
- 🏅 **Excellence Award** · Soongsil University Solved Code Algorithm Competition 2025

<details>
<summary><h2>Explore 8 projects, experiments &amp; tools</h2></summary>

## Projects

### [TrabyOS](https://github.com/TrabyOS) · A spoken request becomes a reviewed trade

**Co-founder & CTO.** A voice trading workspace for web and macOS: ask for market context, review an order, revise it, and approve execution on your exchange account. The product also provides voice technology for partner platforms.

- **Own the path across languages and surfaces.** Python orchestration, Spring Boot services, native Swift UI, and the web experience connect market data, account state, and order workflows.
- **Separate interpretation from execution authority.** Natural language prepares the action; explicit user approval and deterministic checks govern execution. Market identity, quantities, and account state stay part of the transaction contract.
- **Build beyond the conversation.** Exchange integration, real-time updates, onboarding, packaging, and deployment make the system usable outside a development session.

`Python` · `Java / Spring Boot` · `Swift / SwiftUI` · `TypeScript` · `PostgreSQL / WebSocket`

[GitHub organization](https://github.com/TrabyOS)

### ssu Campus AI · Campus services, with a reliable path from intent to action

[ssuAI](https://github.com/ghdtjdwn/ssuAI) · [ssuMCP](https://github.com/ghdtjdwn/ssuMCP) · [ssuAgent](https://github.com/ghdtjdwn/ssuAgent) · [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service)

Students search university information and use their own academic, LMS, and library data through a web app or an agent. I built the **four-service platform**, from connectors and orchestration to deployment and observability.

- **Campus workflows through both a web app and an MCP server.** Expose **52 MCP tools** for university information and academic, LMS, and library tasks, usable from clients such as Claude Desktop and Cursor. REST and MCP share business rules; LangGraph manages specialist routing, persistent conversations, and approval before writes. [MCP connection guide](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/mcp-tools.md)
- **100 competing reservations → 1 upstream write.** An intent queue and same-seat suppression protect the university system. Verified with 100 concurrent requests against WireMock; this is a reduction in external writes, with a deliberate latency trade-off. [Load-test evidence](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/performance/library-agent-load-test.md)
- **Built and operated the delivery path.** ARM64 images move through GitHub Actions, GHCR, and ArgoCD to k3s. Prometheus/Grafana, Tempo, and Loki connect metrics, traces, and logs; fault injection verified circuit-breaker isolation and recovery. [Observability & incident records](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/troubleshooting-highlights.md)

`Java / Spring Boot` · `Python / LangGraph` · `PostgreSQL / Redis` · `k3s / ArgoCD` · `OpenTelemetry`

[Web app](https://ssuai.vercel.app) · [Chat](https://ssuai.vercel.app/chat)

### [marketvalley](https://github.com/unithon26/marketvalley) · One hypothesis, a complete market-validation workflow

**Backend, AI, and platform.** A founder describes a problem and solution once; the team product creates a landing page, **five social cards**, copy, and a Meta ad, then brings back Insights, visits, and consented early-access reservations.

Built the durable workflow behind it: PostgreSQL jobs, `SKIP LOCKED`, leases, operation keys, and checkpoints keep generation, ad creation, and result collection independent of a browser tab, with controlled retries around external side effects. [Architecture](https://github.com/unithon26/marketvalley/blob/main/docs/architecture.md)

🏆 **Manifest Special Award · UNITHON 2026.**

`Next.js` · `Supabase / PostgreSQL` · `Anthropic` · `Meta Marketing API`

[Organization](https://github.com/unithon26) · [Source & team roles](https://github.com/unithon26/marketvalley) · [Live service](https://marketvaley.vercel.app)

### [Geuneul](https://github.com/ghdtjdwn/geuneul) · Find relief from the heat, without waiting on the map

A summer survival map over **150k+ public points of interest**, with nearby shade, shelters, and live community reports. I built the data ingestion, spatial backend, application, and infrastructure.

- **Found the bottleneck in the execution plan.** Spatial indexes were already working; expired reports were still scanned for every scored search. Indexing their expiry filter cut SQL execution time **361 → 172 ms (~52%)** on the same synthetic dataset: 300k places and 210k reports, measured locally under QEMU. [EXPLAIN comparison](https://github.com/ghdtjdwn/geuneul/blob/main/perf/explain/RESULTS.md)
- **Kept data and updates repeatable.** Idempotent ETL, PostGIS radius/nearest-neighbor queries, SSE reports, and infrastructure as code connect ingestion to the map.

`Spring Boot` · `PostgreSQL / PostGIS` · `SSE` · `Terraform / AWS`

[Source & architecture](https://github.com/ghdtjdwn/geuneul) · [Open the map](https://geuneul.vercel.app)

### [Cham Domi](https://github.com/chamdormie) · From dormitory eligibility to an actual roommate group

**Frontend, roommate domain, integration, and application infrastructure.** Built explainable recommendations across **eight lifestyle dimensions**, recruitment/application flows, and one-to-one/group chat. Owned the application's Spring Boot/MySQL deployment, Helm configuration, network isolation, image-digest checks, and backup/restore gates.

🥈 **Silver Prize · Soongsil University CS Software Competition 2026.** The team delivered the dormitory eligibility and roommate experience together.

`Spring Boot` · `Next.js` · `MySQL` · `WebSocket` · `Helm`

[Organization](https://github.com/chamdormie) · [Open the service](https://chamdomi.vercel.app)

### [HeungMap](https://github.com/ghdtjdwn/heungmap) · Turn a forecast into a decision a planner can use

**Backend, data, modeling, and integration.** A tourism-data product that connects festival planning with visitor discovery. The model forecasts **regional visitor-days**, with D−30 information constraints, prediction ranges, and contributing factors.

- **WAPE 4.256% → 3.939%.** A seasonal baseline plus LightGBM residual model improved WAPE by **7.43% relative** on a retrospective time holdout of **4,959 region-days**. [Model card](https://github.com/ghdtjdwn/heungmap/blob/main/docs/MODEL_CARD.md)
- **Forecast coverage 30 → 98 out of 100 real events.** Corrected date-window and administrative-region history handling to make more events usable without changing the prediction target to festival attendance. [Decision record](https://github.com/ghdtjdwn/heungmap/blob/main/docs/DECISION_LOG.md)
- **Keep generated reports grounded.** The API rejects unsupported figures; scheduled retraining only adopts models that pass five acceptance gates.

`FastAPI` · `LightGBM / pandas` · `Next.js` · `Claude` · `Scheduled data pipelines`

[Source](https://github.com/ghdtjdwn/heungmap) · [Live service](https://heungmap.vercel.app)

### [Folding](https://github.com/dotenv-uploaded/_FOLDING_) · Ask across documents; approve the changes

**Agent backend and file-operation boundaries.** A local-first workspace for HWP, Office, and PDF. Built the FastAPI sidecar, agent orchestration, approvals, file edits/undo, and knowledge synchronization. Retrieval exposes source evidence; approved edits produce and verify a new file while preserving the original.

`FastAPI` · `Electron` · `SQLite` · `Local LLM`

[Organization](https://github.com/dotenv-uploaded) · [Product repository](https://github.com/dotenv-uploaded/_FOLDING_) · [Agent backend](https://github.com/dotenv-uploaded/_FOLDING_/tree/main/services/agent) · [Run locally](https://github.com/dotenv-uploaded/_FOLDING_#running-locally)

### [Billit · JECT](https://github.com/JECT-Study/Billit-5th-Infra) · Give a team a repeatable deployment path

**Team infrastructure.** Built the infrastructure foundation for a collaborative product: **three OCI ARM servers** separating production application, production data, and development/monitoring.

- **Build once, promote the same image.** Reusable GitHub Actions workflows build ARM64 images, deploy to development, and support manual promotion to production. Environment-level deployment coordination and health-check rollback protect the delivery path.
- **Include the work after deployment.** OpenTofu, Docker Compose, Nginx, PostgreSQL/Redis, backups, and Prometheus/Loki/Grafana cover provisioning through operations. Deployment and timeout behavior were checked in an isolated integration environment; application rollout is being connected.

`OCI / OpenTofu` · `GitHub Actions / GHCR` · `Docker / Nginx` · `PostgreSQL / Redis` · `Prometheus / Grafana / Loki`

[JECT](https://github.com/JECT-Study) · [Infrastructure](https://github.com/JECT-Study/Billit-5th-Infra) · [Backend](https://github.com/JECT-Study/Billit-5th-Server) · [Frontend](https://github.com/JECT-Study/Billit-5th-Client)

## Earlier work & experiments

| Work | What I worked on |
| :--- | :--- |
| [Macro](https://github.com/UNITHON24/Macro) · [UNITHON24](https://github.com/UNITHON24) | Voice access to existing kiosk software. Reworked fragile coordinate automation into UIA/OCR actions, postcondition checks, and an idempotent SQLite queue; 76 recorded tests and Linux/Windows CI. |
| AI말평 experiments | Compared **19 encoder backbones / 24 configurations** with nested out-of-fold evaluation; further checked finalists with leave-one-prompt-out evaluation and leakage audits under deployment constraints. |
| AXWAR submissions | Built three pipelines for grounded FAQ answers, disclosure summaries, and refund calculation, separating model-generated text from deterministic numeric and evidence validation. |

## Tools I use

| Area | Stack |
| :--- | :--- |
| **Backend & data** | Java · Spring Boot · Python · FastAPI · PostgreSQL/PostGIS · MySQL · Redis |
| **Infrastructure & observability** | Docker · Kubernetes/k3s · ArgoCD · GitHub Actions · Terraform/OpenTofu · AWS/OCI · OpenTelemetry · Prometheus/Grafana · Tempo/Loki |
| **AI & product integration** | LangGraph · MCP · RAG · LightGBM · TypeScript/Next.js · Swift/SwiftUI |

<sub>Performance figures link to their measurement conditions. Project roles distinguish individual ownership from team delivery.</sub>

</details>
