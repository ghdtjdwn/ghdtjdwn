# Seongju Hong

Backend and AI systems engineer. Computer Science student at Soongsil University.
I build services end to end: the data model and API, agent orchestration, deployment, observability, and failure recovery.

[Website](https://seongju.vercel.app) · [Email](mailto:seongjuice999@gmail.com) · [한국어](./README_KR.md)

## Experience

- **Founding Engineer, [TrabyOS](https://github.com/TrabyOS)** · Sep 2026 ~ present. Technical owner of a voice-first AI trading workspace for macOS, from deterministic trade resolution to the native voice interface. [Website](https://trabyos-website.vercel.app/) · [Free test build](https://github.com/TrabyOS/trabyos-test/releases/latest)
- **Software Engineer Intern, [Bizarre Cube AI](https://www.bzrr.ai/)** · [MXN Commerce Group](https://www.mxncommerce.com/en) · Sep 2026 ~ present. Production AI agents for fashion e-commerce operations. [GitHub](https://github.com/bizarrecube)
- **Republic of Korea Army** · May 2023 ~ Nov 2024. Mandatory military service.
- **Soongsil University**, School of Computer Science & Engineering · 2022 ~ present. [Coursework](https://github.com/ghdtjdwn/cs-coursework)

## Projects

- **ssu Campus AI Platform** `Spring Boot` `LangGraph` `Next.js` `Kubernetes`
  Soongsil University's public and personal academic, LMS, and library data through a web app, a natural-language agent, and 52 approval-aware MCP tools. The platform is split into [ssuAI](https://github.com/ghdtjdwn/ssuAI), [ssuMCP](https://github.com/ghdtjdwn/ssuMCP), [ssuAgent](https://github.com/ghdtjdwn/ssuAgent), and [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service), deployed to ARM64 Kubernetes with end-to-end observability. [Web](https://ssuai.vercel.app)
- **[Geuneul](https://github.com/ghdtjdwn/geuneul)** `Spring Boot` `PostGIS` `AWS → OCI` `Terraform`
  A summer survival map for 150k+ public POIs, with GiST-backed radius and kNN search and real-time reports over LISTEN/NOTIFY and SSE. The repository records the current data-preserving migration from AWS to OCI. [Web](https://geuneul.vercel.app)
- **[Cham Domi](https://github.com/chamdormie)** `Spring Boot` `Next.js` `MySQL` `k3s`
  Dormitory discovery, explainable roommate matching, and chat. The matching engine implements Irving's Stable Roommates algorithm and is checked against a brute-force oracle. [Web](https://chamdomi.vercel.app)
- **[marketvalley](https://github.com/unithon26/marketvalley)** `Next.js` `Supabase` `Meta Marketing API`
  One idea becomes a landing page, five social cards, Meta ads, and a report grounded in actual visits, reservations, and Insights. Long-running work survives a closed browser through a leased PostgreSQL state machine. [Web](https://marketvaley.vercel.app) · [Team](https://github.com/unithon26)
- **[Folding](https://github.com/dotenv-uploaded/_FOLDING_)** `FastAPI` `Gemma 4` `Electron` `SQLite`
  A local-first document agent for HWP, Office, and PDF. Its evidence-backed knowledge graph connects files by shared entities; exact-diff approval, source-hash checks, atomic replacement, and undo keep edits reviewable and recoverable. [Team](https://github.com/dotenv-uploaded)
- **[HeungMap](https://github.com/ghdtjdwn/heungmap)** `FastAPI` `LightGBM` `Next.js` `Claude`
  Festival demand forecasting on Korea Tourism Organization open data. A seasonal baseline plus LightGBM residual model reached 3.9% WAPE on a time holdout; generated planning reports reject figures absent from the model input.

## Open source

Merged upstream. [All PRs on GitHub](https://github.com/search?q=is%3Apr+author%3Aghdtjdwn+-org%3Aghdtjdwn&type=pullrequests)

- **[psycopg](https://github.com/psycopg/psycopg)** `Python` · `AsyncConnectionPool.getconn()` could swallow task cancellation during a connection check and hang worker shutdown (hit in Procrastinate). Reproduced it, wrote a deterministic regression test, and verified the fix at the maintainer's request before the issue was closed. [#1345](https://github.com/psycopg/psycopg/issues/1345) · [PR #1407](https://github.com/psycopg/psycopg/pull/1407)
- **[Ouroboros](https://github.com/Q00/ouroboros)** `Python` · Cancelling an in-progress MCP client connect left the adapter marked connected with its HTTP client open. Reset state and release owned resources before re-raising, with six regression tests. Approved by two maintainers. [#2364](https://github.com/Q00/ouroboros/issues/2364) · [PR #2365](https://github.com/Q00/ouroboros/pull/2365)
- **[Caveman](https://github.com/JuliusBrussee/caveman)** `Go` · `--force` never refreshed editor rule files once a repo was initialized, so rule updates could not reach `.cursor`, `.windsurf`, or `.clinerules`. One-character fix with red-first tests; the maintainer called it "a one-character bug with real reach". [PR #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · merged via [#1015](https://github.com/JuliusBrussee/caveman/pull/1015) with authorship preserved


## Awards

- 🏆 Manifest Special Award · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 Silver Prize · Soongsil University CS Software Competition 2026 · [Cham Domi](https://github.com/chamdormie)
- 🏅 Excellence Award · Soongsil University Solved Code Algorithm Competition 2025

## Stack

Java, Kotlin, Spring Boot · Python, FastAPI, LangGraph, MCP · TypeScript, Next.js · Swift, macOS · PostgreSQL, PostGIS, Redis, Kafka · Docker, Kubernetes, Argo CD, Terraform, AWS, OCI · Prometheus, Grafana, Tempo, Loki, OpenTelemetry
