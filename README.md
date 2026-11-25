**I build backend systems, infrastructure, and AI products - with concurrency, observability, and recovery designed in.**

[LinkedIn](https://www.linkedin.com/in/ghdtjdwn/) · [Email](mailto:seongjuice999@gmail.com) · [한국어](./README_KR.md)

## Experience

- [Bizarre Cube AI](https://www.bzrr.ai/) Software Engineer Intern (2026.09 ~ ) · [Organization](https://github.com/bizarrecube)
- [JECT](https://ject.kr/) Backend & Infrastructure Engineer (2026.10 ~ ) · [My PRs](https://github.com/JECT-Study/Billit-5th-Server/pulls?q=is%3Apr+author%3Aghdtjdwn+is%3Amerged) · [Infrastructure](https://github.com/JECT-Study/Billit-5th-Infra)
- [TrabyOS](https://github.com/TrabyOS) Founding team, Technical Lead (2026.09 ~ 2026.10)
- Soongsil University Computer Science (2022.03 ~ 2027.02, expected) · [Coursework across 12 subjects](https://github.com/ghdtjdwn/cs-coursework)
- Republic of Korea Army Military Service (2023.05 ~ 2024.11)

## Open source

10 pull requests merged or adopted in 6 external repositories, mostly observability, cancellation, and regression tests.

| Project | What I changed | Status |
|---|---|---|
| [OpenTelemetry Python](https://github.com/open-telemetry/opentelemetry-python/pulls?q=is%3Apr+author%3Aghdtjdwn) | `CapturingSampler`, the shared test sampler a maintainer [asked for](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5073#discussion_r4061037725); the tests of 18 contrib packages now use it | Released in 1.45.0 · [#5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681) |
| [OpenTelemetry Python Contrib](https://github.com/open-telemetry/opentelemetry-python-contrib/pulls?q=is%3Apr+author%3Aghdtjdwn) | Request headers available at sampling time (WSGI), header masking gap found in review (Tornado), default timeout kept (urllib), client span attributes at creation (Tornado), header-capture docs (Starlette) | Merged · [#5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032) · [#5170](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5170) · [#5347](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5347) · [#5348](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5348) · [#5356](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5356) |
| [Micrometer](https://github.com/micrometer-metrics/micrometer) | Custom tags for Java HttpClient observations, with examples the test suite compiles and runs | Released in 1.16.8 · 1.17.2 · [#7925](https://github.com/micrometer-metrics/micrometer/pull/7925) |
| [Ouroboros](https://github.com/Q00/ouroboros) | HTTP resources and connection state released when MCP initialization is cancelled, with six regression cases | v0.54.5 · [#2365](https://github.com/Q00/ouroboros/pull/2365) |
| [Ponytail](https://github.com/DietrichGebert/ponytail) | The selected branch's saved mode returns after conversation-tree navigation | v4.13.0 · [#828](https://github.com/DietrichGebert/ponytail/pull/828) |
| [Caveman](https://github.com/JuliusBrussee/caveman) | Forced rule updates | Cherry-picked into v2.7.0 · [#1013](https://github.com/JuliusBrussee/caveman/pull/1013) |

Also reproduced a swallowed cancellation in [psycopg #1345](https://github.com/psycopg/psycopg/issues/1345) and verified the maintainer's fix (psycopg_pool 3.3.2).

**In review** · [OpenTelemetry](https://github.com/open-telemetry/opentelemetry-python-contrib/pulls?q=is%3Apr+is%3Aopen+author%3Aghdtjdwn) · [Lettuce #3909](https://github.com/redis/lettuce/pull/3909) · [Spring AI #6929](https://github.com/spring-projects/spring-ai/pull/6929) · [slowapi #305](https://github.com/laurentS/slowapi/pull/305)

## Awards

- 🏅 **Excellence Award** · 2026 Tourism Data Utilization Contest, Web & App track · Korea Tourism Organization · [HeungMap](https://github.com/ghdtjdwn/heungmap)
- 🏆 **Manifest Special Award** · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 **Silver Prize** · Soongsil University CS Software Competition 2026 · [Cham Domi](https://github.com/chamdormie)
- 🏅 **Excellence Award** · Soongsil University Solved Code Algorithm Competition 2025

## Projects

- **[ssu Campus AI](https://github.com/ghdtjdwn/ssuMCP)** · Soongsil campus services through a web app and 52 MCP tools; four services built and operated alone. **100 concurrent reservations for one seat → 1 upstream write.** [Load test](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/performance/library-agent-load-test.md) · [Web app](https://ssuai.vercel.app)
- **[HeungMap](https://github.com/ghdtjdwn/heungmap)** · Regional visitor-demand forecasts for festival planners. **WAPE 4.256% → 3.939%** on a time holdout of 4,959 region-days. [Model card](https://github.com/ghdtjdwn/heungmap/blob/main/docs/MODEL_CARD.md) · [Live service](https://heungmap.vercel.app)
- **[Geuneul](https://github.com/ghdtjdwn/geuneul)** · A heat-relief map over 150k+ public places with live reports. **Scored-search SQL 361 ms → 172 ms** on a synthetic 300k-place dataset, measured locally. [EXPLAIN comparison](https://github.com/ghdtjdwn/geuneul/blob/main/perf/explain/RESULTS.md) · [Open the map](https://geuneul.vercel.app)
- **[marketvalley](https://github.com/unithon26/marketvalley)** · One startup idea becomes a landing page, social cards, and a Meta ad with real results. Durable PostgreSQL jobs with `SKIP LOCKED`, leases, and checkpoints. [Architecture](https://github.com/unithon26/marketvalley/blob/main/docs/architecture.md)
- **[Cham Domi](https://github.com/chamdormie)** · Dormitory roommate matching across eight lifestyle dimensions, with recruitment and chat. Frontend, roommate domain, and application deployment. [Open the service](https://chamdomi.vercel.app)

<sub>Performance figures link to their measurement conditions. Team projects name my part.</sub>
