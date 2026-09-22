# Seongju Hong

Backend and AI systems engineer studying Computer Science at Soongsil University.
I build products where model output meets real data, explicit user decisions, and systems that must keep working after the demo.

[Website](https://seongju.vercel.app) · [Email](mailto:seongjuice999@gmail.com) · [한국어](./README_KR.md)

## Now

- **Founding Engineer at [TrabyOS](https://github.com/TrabyOS)** · A voice-first trading workspace for macOS. Users ask for live market context, review a complete order card, and approve, correct, or cancel a paper trade by voice. [Website](https://trabyos-website.vercel.app/) · [Free test build](https://github.com/TrabyOS/trabyos-test/releases/latest)
- **Software Engineer Intern at [Bizarre Cube AI](https://www.bzrr.ai/), [MXN Commerce Group](https://www.mxncommerce.com/en)** · Production AI agents for fashion e-commerce operations. [GitHub](https://github.com/bizarrecube)
- **B.S. in Computer Science, Soongsil University** · 2022–present. [Coursework](https://github.com/ghdtjdwn/cs-coursework)

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

## Open source

Merged upstream work. [Browse all pull requests](https://github.com/search?q=is%3Apr+author%3Aghdtjdwn+-org%3Aghdtjdwn&type=pullrequests)

- [psycopg #1407](https://github.com/psycopg/psycopg/pull/1407) · Reproduced a swallowed cancellation in `AsyncConnectionPool.getconn()` and added a deterministic regression test; verified the final fix with the maintainer.
- [Ouroboros #2365](https://github.com/Q00/ouroboros/pull/2365) · Fixed cancellation cleanup for an in-progress MCP client connection and added six regression tests.
- [Caveman #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · Fixed `--force` failing to refresh editor rule files after initialization; authorship was preserved in the merged follow-up.

## Awards

- 🏆 Manifest Special Award · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 Silver Prize · Soongsil University CS Software Competition 2026 · [Cham Domi](https://github.com/chamdormie)
- 🏅 Excellence Award · Soongsil University Solved Code Algorithm Competition 2025
