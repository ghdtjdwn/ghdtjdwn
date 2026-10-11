# Seongju Hong

Backend and AI systems engineer studying Computer Science at Soongsil University.
I build products where model output meets real data, explicit user decisions, and systems that must keep working after the demo.

[Website](https://seongju.vercel.app) · [Email](mailto:seongjuice999@gmail.com) · [한국어](./README_KR.md)

## Now

- **Founding Engineer at [TrabyOS](https://github.com/TrabyOS)** · A voice trading assistant that places real crypto trades. Say an order for spot or perpetual futures, and TrabyOS shows it as an order card and executes it on the exchange once you approve. You can also ask for prices, your balance, or the news. [Website](https://trabyos-website.vercel.app/)
- **Software Engineer Intern at [Bizarre Cube AI](https://www.bzrr.ai/) ([MXN Commerce Group](https://www.mxncommerce.com/en))** · Production AI agents for fashion e-commerce operations. [GitHub](https://github.com/bizarrecube)
- **B.S. in Computer Science, Soongsil University** · 2022–present. [Coursework](https://github.com/ghdtjdwn/cs-coursework)

## Awards

- 🏆 Manifest Special Award · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 Silver Prize · Soongsil University CS Software Competition 2026 · [Cham Domi](https://github.com/chamdormie)
- 🏅 Excellence Award · Soongsil University Solved Code Algorithm Competition 2025

## Open source

Six changes merged into upstream projects, plus one fix I reproduced and verified for a maintainer. Ordered from the most involved work to the smallest fix. [Browse all pull requests](https://github.com/search?q=is%3Apr+author%3Aghdtjdwn+-org%3Aghdtjdwn&type=pullrequests)

- **[OpenTelemetry Python Contrib #5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032)** · Request headers for sampling decisions in WSGI

  The WSGI middleware collected request headers only after the server span had been created, so a sampler could not use them. The configured, sanitized headers are now passed in when the span is created, and they still stay out of internal spans and metrics. Merged after a month of review with three approvals; it covers the WSGI item of a maintainer's tracking issue, [#4975](https://github.com/open-telemetry/opentelemetry-python-contrib/issues/4975).

- **[OpenTelemetry Python #5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681)** · A shared `CapturingSampler` for instrumentation tests

  While reviewing the change above, a maintainer asked for one common sampler in place of a test double in every instrumentation. I added it to `opentelemetry-test-utils` in the core repository, where tests use it to check the attributes a sampler receives at span start. Released with 1.45.0 and since picked up by the Django instrumentation tests.

- **[Ouroboros #2365](https://github.com/Q00/ouroboros/pull/2365)** · Cleanup when an MCP client connection is cancelled

  Cancelling `MCPClientAdapter.connect()` midway left the adapter marked as connected and its HTTP client open. I found this and reported it in [#2364](https://github.com/Q00/ouroboros/issues/2364). The fix resets the state and closes the owned client before the cancellation propagates, even if another cleanup step fails. Six regression tests, two maintainer approvals, released in v0.54.5.

- **[psycopg #1345](https://github.com/psycopg/psycopg/issues/1345)** · Reproduction and fix verification for a cancellation lost in the async pool

  `AsyncConnectionPool.getconn()` could swallow a cancellation raised during the connection check and hand a connection to a caller that had already been cancelled. I reproduced the report with instrumentation, shared a deterministic regression test, and confirmed at the maintainer's request that the fix in [#1407](https://github.com/psycopg/psycopg/pull/1407) resolves it. The fix is the maintainer's and shipped in psycopg_pool 3.3.2.

- **[Micrometer #7925](https://github.com/micrometer-metrics/micrometer/pull/7925)** · Reference docs for custom tags on Java `HttpClient` observations

  Resolved a documentation request that had been open since 2024, [#4962](https://github.com/micrometer-metrics/micrometer/issues/4962). The new section shows how to add tags through an `HttpClientObservationConvention` while keeping the default ones. Its snippets come from a test that sends a request and checks the recorded timer, so the example is compiled and tested with the project.

- **[Ponytail #828](https://github.com/DietrichGebert/ponytail/pull/828)** · Mode restored after `/tree` navigation in the Pi extension

  After `/ponytail off`, going back to an earlier branch with `/tree` left Ponytail disabled, because the extension restored the saved mode only at session start. It now does the same on tree navigation, so the injected instructions and the status bar follow the selected branch. Released in v4.13.0.

- **[Caveman #1013](https://github.com/JuliusBrussee/caveman/pull/1013)** · `--force` now refreshes existing editor rule files

  On a repository that was already initialized, `caveman-init --force` reported the Cursor, Windsurf, and Cline rule files as installed and left stale rules in place. A one-character fix with three regression tests. The maintainer cherry-picked my commit into [#1015](https://github.com/JuliusBrussee/caveman/pull/1015), and it was released in v2.7.0.

## Products

### [ssu Campus AI](https://github.com/ghdtjdwn/ssuAI)

Students can search university information and work with their own academic, LMS, and library data from one web app or natural-language agent. The system exposes 52 MCP tools with an explicit approval boundary and runs across [ssuAI](https://github.com/ghdtjdwn/ssuAI), [ssuMCP](https://github.com/ghdtjdwn/ssuMCP), [ssuAgent](https://github.com/ghdtjdwn/ssuAgent), and [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service). [Open the service](https://ssuai.vercel.app)

`Spring Boot` `LangGraph` `Next.js` `Kubernetes`

### [Geuneul](https://github.com/ghdtjdwn/geuneul)

A summer survival map that finds nearby shade and heat-relief facilities among 150k+ public points of interest. Radius and nearest-neighbor search are backed by PostGIS, while live community reports arrive without refreshing the map. [Open the map](https://geuneul.vercel.app)

`Spring Boot` `PostGIS` `SSE` `Terraform`

### [Cham Domi](https://github.com/chamdormie)

Students compare their circumstances with dormitory admission rules, see why a requirement passes or fails, and then continue into roommate discovery. Eight lifestyle dimensions power explainable recommendations; recruitment posts, applications, approvals, one-to-one chat, and group chat turn a recommendation into an actual room. [Open Cham Domi](https://chamdomi.vercel.app)

`Spring Boot` `Next.js` `MySQL` `WebSocket`

### [marketvalley](https://github.com/unithon26)

An early founder describes a problem and solution once. The service creates a public landing page, five social cards, copy, and a Meta ad from one validation hypothesis, then returns actual Insights, visits, and consented reservations for the founder's next decision. [Open the service](https://marketvaley.vercel.app) · [Source](https://github.com/unithon26/marketvalley)

`Next.js` `Supabase` `Anthropic` `Meta Marketing API`

### [Folding](https://github.com/dotenv-uploaded)

A local-first desktop workspace for HWP, Office, and PDF. Users ask across a folder, inspect source evidence and document relationships, then approve format-aware edits that create and verify a new file instead of silently overwriting the original. [Source](https://github.com/dotenv-uploaded/_FOLDING_)

`Electron` `FastAPI` `Gemma 4` `SQLite`

### [HeungMap](https://github.com/ghdtjdwn/heungmap)

A planning and discovery service built from Korea Tourism Organization data. It forecasts city- or county-wide visitor-days available 30 days before a festival—not festival attendance—and shows planners a range, contributing factors, and what-if comparisons. The adopted seasonal baseline plus LightGBM residual model reached 3.939% WAPE on a time holdout; generated reports reject figures absent from the model input.

`FastAPI` `LightGBM` `Next.js` `Claude`
