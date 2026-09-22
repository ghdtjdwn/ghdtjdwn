# Seongju Hong

Backend and AI systems engineer. Computer Science student at Soongsil University.
I build services end to end: the data model and API, agent orchestration, deployment, observability, and failure recovery.

[Email](mailto:seongjuice999@gmail.com) · [한국어](./README_KR.md)

## Experience

- **Founding Engineer, [TrabyOS](https://trabyos-website.vercel.app/)** · Sep 2026 ~ present. The startup's only developer. I build the whole voice-first AI trading workspace alone: Spring Boot core, Python coordinator, Swift native voice client, deterministic instrument resolution, and explicit approval before any order.
- **Software Engineer Intern, [Bizarre Cube AI](https://www.bzrr.ai/)** ·([MXN Commerce Group](https://www.mxncommerce.com/en)) · Sep 2026 ~ present. Production AI agents for fashion e-commerce operations.
- **Republic of Korea Army** · May 2023 ~ Nov 2024. Mandatory military service.
- **Soongsil University**, School of Computer Science & Engineering · 2022 ~ present.

## Projects

- **ssu Campus AI Platform** `Spring Boot` `LangGraph` `Next.js` `Kubernetes`
  Soongsil University's public and personal academic, LMS, and library data, served through a web app, a natural-language agent, and 52 MCP tools. Four services that I designed and operate: [ssuAI](https://github.com/ghdtjdwn/ssuAI) (web, same-origin BFF, SSE), [ssuMCP](https://github.com/ghdtjdwn/ssuMCP) (domain tools, REST, approval-gated writes), [ssuAgent](https://github.com/ghdtjdwn/ssuAgent) (LangGraph routing, PostgreSQL checkpoints, human-in-the-loop), and [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service) (embedding gateway). PostgreSQL is the source of truth, Redis handles coordination and rate limits, Kafka handles fan-out, and Argo CD delivers to ARM64 Kubernetes with Prometheus, Tempo, Loki, and Grafana. [Live](https://ssuai.vercel.app)
- **[Geuneul](https://github.com/ghdtjdwn/geuneul)** `Spring Boot` `PostGIS` `AWS ECS` `Terraform`
  A summer survival map: 150k+ public POIs, radius and kNN search on PostGIS, and real-time user reports over LISTEN/NOTIFY and SSE. Solo project. Terraform-declared AWS, OIDC deploys from GitHub Actions, k6 load tests, and tuning decided from EXPLAIN plans. [Live](https://geuneul.vercel.app)
- **Cham Domi** `Spring Boot` `Next.js` `MySQL` `k3s`
  Dormitory discovery with explainable roommate matching and chat, built by a team of three. My part: the frontend, the roommate matching backend (Irving's Stable Roommates checked against a brute-force oracle), chat with MySQL as the authority, and the k3s/Helm production infrastructure. [Live](https://chamdomi.vercel.app)
- **[marketvalley](https://github.com/unithon26/marketvalley)** `Next.js` `Supabase` `Meta Marketing API`
  Automated market validation: one idea in, a landing page, card news, Meta ads, and a real-response report out. My part: backend and AI, the content pipeline, per-user data isolation, long-running jobs, and the Meta Ads integration. [Live](https://marketvaley.vercel.app)
- **[Folding](https://github.com/dotenv-uploaded/_FOLDING_)** `FastAPI` `Claude Agent SDK` `Electron` `SQLite`
  A local-first document agent that reads, connects, and safely edits HWP, Office, and PDF files while preserving evidence from the originals. Team of four. My part: the entire AI agent runtime and the knowledge graph. The runtime is a FastAPI sidecar built on the Claude Agent SDK where the model gets no write tools, every change is previewed as an exact diff and hash-approved by the user, and files are replaced atomically with crash-recoverable journals and undo. The knowledge graph derives relationships between converted documents from shared entities, keeps the supporting sentence from each source as evidence, and is rebuilt as an immutable version after every verified change.
- **[HeungMap](https://github.com/ghdtjdwn/heungmap)** `FastAPI` `LightGBM` `Next.js` `Claude`
  Festival demand forecasting on Korea Tourism Organization open data, entered in the 2026 Tourism Data Contest. Lead developer in a team of two. My part: the D-30 regional visitor model (seasonal baseline plus LightGBM residuals, WAPE 3.9% on a time holdout), the FastAPI service, Claude-written planning reports with server-side checks that reject numbers absent from the input, daily retraining on an Oracle Cloud cron, and the Next.js planner and visitor web app.

## Open source

Mostly cancellation, races, and lost state in concurrent runtimes, each starting from a reproduction and a failing test. [All PRs on GitHub](https://github.com/search?q=is%3Apr+author%3Aghdtjdwn+-org%3Aghdtjdwn&type=pullrequests)

**Merged upstream**

- **[psycopg](https://github.com/psycopg/psycopg)** `Python` · `AsyncConnectionPool.getconn()` could swallow task cancellation during a connection check and hang worker shutdown. Reproduced it, wrote a deterministic regression test, and verified the maintainer's fix. [#1345](https://github.com/psycopg/psycopg/issues/1345) · [PR #1407](https://github.com/psycopg/psycopg/pull/1407)
- **[Ouroboros](https://github.com/Q00/ouroboros)** `Python` · Cancelling an in-progress MCP client connect left the adapter marked connected with its HTTP client open. Reset state and release owned resources before re-raising, with six regression tests. [#2364](https://github.com/Q00/ouroboros/issues/2364) · [PR #2365](https://github.com/Q00/ouroboros/pull/2365)
- **[Caveman](https://github.com/JuliusBrussee/caveman)** `Go` · `--force` never refreshed editor rule files once a repo was initialized. One-character fix with red-first tests. [PR #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · merged via [#1015](https://github.com/JuliusBrussee/caveman/pull/1015)

**Under review**

- **[OpenTelemetry Python](https://github.com/open-telemetry/opentelemetry-python-contrib)** `Python` · WSGI SERVER spans received captured request headers only after sampling, so samplers could not use them. Pass the configured, sanitized headers as initial span attributes while keeping them out of INTERNAL spans and metrics; the shared `CapturingSampler` test utility requested in review goes to the core repository. [contrib PR #5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032) · [core PR #5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681)
- **[Lettuce](https://github.com/redis/lettuce)** `Java` · A concurrent `setOptions()` could mix configurations during connection initialization. Pass captured `ClientOptions` through `RedisClient`, `RedisClusterClient`, and the shared handshake, including custom factory hooks and asynchronous retries; the maintainer proposed widening this into an explicit `ClientOptions` parameter on the public connection-factory API. [#3591](https://github.com/redis/lettuce/issues/3591) · [PR #3909](https://github.com/redis/lettuce/pull/3909)
- **[Spring AI](https://github.com/spring-projects/spring-ai)** `Java` · A custom `ChatMemory` bean that depends on `RedisChatMemoryRepository` blocked the repository's auto-configuration and failed context startup. Narrow the missing-bean condition to `ChatMemoryRepository`, with integration tests for custom memory, custom repository precedence, and the default memory. [#6926](https://github.com/spring-projects/spring-ai/issues/6926) · [PR #6929](https://github.com/spring-projects/spring-ai/pull/6929)
- **[SlowAPI](https://github.com/laurentS/slowapi)** `Python` · Endpoints were keyed by module and `__name__`, so same-named class methods such as `First.index` and `Second.index` shared one rate limit and one exemption. Use `__qualname__` for registration, lookup, exemptions, and middleware matching, with 18 regression cases. [#173](https://github.com/laurentS/slowapi/issues/173) · [PR #305](https://github.com/laurentS/slowapi/pull/305)
- **[Micrometer](https://github.com/micrometer-metrics/micrometer)** `Java` · Documented custom tags for Java `HttpClient` observations through `HttpClientObservationConvention`, with examples taken from a compiled test. [#4962](https://github.com/micrometer-metrics/micrometer/issues/4962) · [PR #7925](https://github.com/micrometer-metrics/micrometer/pull/7925)

## Awards

- 🏆 Manifest Special Award · UNITHON 2026 · marketvalley
- 🥈 Silver Prize · Soongsil University CS Software Competition 2026 · Cham Domi
- 🏅 Excellence Award · Soongsil University Solved Code Algorithm Competition 2025

## Stack

Java, Kotlin, Spring Boot · Python, FastAPI, LangGraph, MCP · TypeScript, Next.js · PostgreSQL, PostGIS, Redis, Kafka · Docker, Kubernetes, Argo CD, Terraform, AWS · Prometheus, Grafana, Tempo, Loki, OpenTelemetry
