**I build backend systems, infrastructure, and AI products - with concurrency, observability, and recovery designed in.**

[LinkedIn](https://www.linkedin.com/in/ghdtjdwn/) · [Email](mailto:seongjuice999@gmail.com) · [한국어](./README_KR.md)

## Experience

- [Bizarre Cube AI](https://www.bzrr.ai/) Software Engineer Intern (2026.09 ~ ) · [Organization](https://github.com/bizarrecube)
- [JECT](https://ject.kr/) Backend & Infrastructure Engineer (2026.09 ~ ) · [Backend](https://github.com/JECT-Study/Billit-5th-Server) · [My PRs](https://github.com/JECT-Study/Billit-5th-Server/pulls?q=is%3Apr+author%3Aghdtjdwn) · [Infrastructure](https://github.com/JECT-Study/Billit-5th-Infra)
- [TrabyOS](https://github.com/TrabyOS) Co-founder & CTO (2026.07 ~ 2026.10)
- Soongsil University Computer Science (2022.03 ~ ) · [Coursework across 12 subjects](https://github.com/ghdtjdwn/cs-coursework)
- Republic of Korea Army Military Service (2023.05 ~ 2024.11)

## Open source

I contribute upstream where my own systems depend on it: observability, cancellation, and regression tests.

### [OpenTelemetry Python](https://github.com/open-telemetry/opentelemetry-python-contrib/pulls?q=is%3Apr+author%3Aghdtjdwn) · From one instrumentation bug to shared test infrastructure

- **A shared test sampler, requested by a maintainer.** A maintainer [asked for one sampler in the core test utilities](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5073#discussion_r4061037725) instead of a copy in each instrumentation. I implemented `CapturingSampler`; it shipped in **1.45.0** and the tests of **18 contrib packages** now use it. [Core #5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681) · [Adoption example](https://github.com/open-telemetry/opentelemetry-python-contrib/blob/de43f819a4a919213d246a23e62a1b256aeca7b9/instrumentation/opentelemetry-instrumentation-asgi/tests/test_asgi_custom_headers.py)
- **Headers available when sampling happens.** WSGI passes sanitized request headers at span creation and keeps them out of internal spans and metrics. Merged with three maintainer approvals. [Contrib #5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032)
- **A masking gap found in review.** While reviewing six follow-up PRs for [#4975](https://github.com/open-telemetry/opentelemetry-python-contrib/issues/4975), I found Tornado ignoring the sensitive-header masking settings and fixed it with the shared capture helper. [Contrib #5170](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5170) · [Review of #5163](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5163)

### Reliability fixes in other projects

- **[Ouroboros #2365](https://github.com/Q00/ouroboros/pull/2365) · Cancellation cleanup** - merged, v0.54.5. HTTP resources and connection state are released when MCP initialization is cancelled, with six regression cases.
- **[Micrometer #7925](https://github.com/micrometer-metrics/micrometer/pull/7925) · Tested observability documentation** - merged. Custom tags for Java HttpClient observations, with examples the test suite compiles and runs.
- **[psycopg #1345](https://github.com/psycopg/psycopg/issues/1345) · Async pool cancellation** - reproduction and verification. Reproduced a swallowed cancellation, proposed a deterministic regression test, and confirmed the maintainer's fix, shipped in psycopg_pool 3.3.2.
- **[Ponytail #828](https://github.com/DietrichGebert/ponytail/pull/828) · Branch state restoration** - merged, v4.13.0. The selected branch's saved mode returns after conversation-tree navigation.
- **[Caveman #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · Forced rule updates** - adopted in v2.7.0. The maintainer cherry-picked the fix into [#1015](https://github.com/JuliusBrussee/caveman/pull/1015).

**In review** · [OpenTelemetry](https://github.com/open-telemetry/opentelemetry-python-contrib/pulls?q=is%3Apr+is%3Aopen+author%3Aghdtjdwn) · [Lettuce #3909](https://github.com/redis/lettuce/pull/3909) · [Spring AI #6929](https://github.com/spring-projects/spring-ai/pull/6929) · [slowapi #305](https://github.com/laurentS/slowapi/pull/305)

## Awards

- 🏅 **Excellence Award** · 2026 Tourism Data Utilization Contest, Web & App track · Korea Tourism Organization · [HeungMap](https://github.com/ghdtjdwn/heungmap)
- 🏆 **Manifest Special Award** · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 **Silver Prize** · Soongsil University CS Software Competition 2026 · [Cham Domi](https://github.com/chamdormie)
- 🏅 **Excellence Award** · Soongsil University Solved Code Algorithm Competition 2025

## Projects

- **100 concurrent requests for one seat → 1 upstream write** · [ssu Campus AI](https://github.com/ghdtjdwn/ssuMCP) · [Load test](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/performance/library-agent-load-test.md)
- **WAPE 4.256% → 3.939%** on a time holdout of 4,959 region-days · [HeungMap](https://github.com/ghdtjdwn/heungmap) · [Model card](https://github.com/ghdtjdwn/heungmap/blob/main/docs/MODEL_CARD.md)
- **361 ms → 172 ms** scored-search SQL on a synthetic 300k-place dataset, measured locally · [Geuneul](https://github.com/ghdtjdwn/geuneul) · [EXPLAIN comparison](https://github.com/ghdtjdwn/geuneul/blob/main/perf/explain/RESULTS.md)

<details>
<summary><b>Explore all 7 projects</b></summary>

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
- **Built and operated the delivery path.** ARM64 images are built in GitHub Actions and published to GHCR. Until October 2026 ArgoCD rolled them out to k3s, with Prometheus/Grafana, Tempo, and Loki connecting metrics, traces, and logs; fault injection verified circuit-breaker isolation and recovery. To fit a free-tier budget, I then moved the services to one VM running Docker Compose, where a timer pulls the newest image, checks public health, and rolls back on failure. [Observability & incident records](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/troubleshooting-highlights.md) · [Platform decision](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/adr/0101-single-vm-docker-compose-timer-pull.md)

`Java / Spring Boot` · `Python / LangGraph` · `PostgreSQL / Redis` · `Docker Compose / GHCR` · `OpenTelemetry`

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

`Spring Boot` · `PostgreSQL / PostGIS` · `SSE` · `Terraform / Oracle Cloud`

[Source & architecture](https://github.com/ghdtjdwn/geuneul) · [Open the map](https://geuneul.vercel.app)

### [Cham Domi](https://github.com/chamdormie) · From dormitory eligibility to an actual roommate group

**Frontend, roommate domain, integration, and application infrastructure.** Built explainable recommendations across **eight lifestyle dimensions**, recruitment/application flows, and one-to-one/group chat. Owned the application's Spring Boot/MySQL deployment, Helm configuration, network isolation, image-digest checks, and backup/restore gates.

🥈 **Silver Prize · Soongsil University CS Software Competition 2026.** The team delivered the dormitory eligibility and roommate experience together.

`Spring Boot` · `Next.js` · `MySQL` · `WebSocket` · `Helm`

[Organization](https://github.com/chamdormie) · [Open the service](https://chamdomi.vercel.app)

### [HeungMap](https://github.com/ghdtjdwn/heungmap) · Turn a forecast into a decision a planner can use

**Backend, data, modeling, and integration.** A tourism-data product that connects festival planning with visitor discovery. The model forecasts **regional visitor-days**, with D−30 information constraints, prediction ranges, and contributing factors.

🏅 **Excellence Award · 2026 Tourism Data Utilization Contest (Korea Tourism Organization).**

- **WAPE 4.256% → 3.939%.** A seasonal baseline plus LightGBM residual model improved WAPE by **7.43% relative** on a retrospective time holdout of **4,959 region-days**. [Model card](https://github.com/ghdtjdwn/heungmap/blob/main/docs/MODEL_CARD.md)
- **Forecast coverage 30 → 98 out of 100 real events.** Corrected date-window and administrative-region history handling to make more events usable without changing the prediction target to festival attendance. [Decision record](https://github.com/ghdtjdwn/heungmap/blob/main/docs/DECISION_LOG.md)
- **Keep generated reports grounded.** The API rejects unsupported figures; scheduled retraining adopts models that pass five acceptance gates, and falls back to a clearly flagged provisional model only when the current one is about to expire.

`FastAPI` · `LightGBM / pandas` · `Next.js` · `Claude` · `Scheduled data pipelines`

[Source](https://github.com/ghdtjdwn/heungmap) · [Live service](https://heungmap.vercel.app)

### [Folding](https://github.com/dotenv-uploaded/_FOLDING_) · Ask across documents; approve the changes

**Agent backend and file-operation boundaries.** A local-first workspace for HWP, Office, and PDF. Built the FastAPI sidecar, agent orchestration, approvals, file edits/undo, and knowledge synchronization. Retrieval exposes source evidence; approved edits produce and verify a new file while preserving the original.

`FastAPI` · `Electron` · `SQLite` · `Local LLM`

[Organization](https://github.com/dotenv-uploaded) · [Product repository](https://github.com/dotenv-uploaded/_FOLDING_) · [Agent backend](https://github.com/dotenv-uploaded/_FOLDING_/tree/main/services/agent) · [Run locally](https://github.com/dotenv-uploaded/_FOLDING_#running-locally)

<sub>Performance figures link to their measurement conditions. Project roles distinguish individual ownership from team delivery.</sub>

</details>
