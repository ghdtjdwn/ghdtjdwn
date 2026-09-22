# Seongju Hong

Backend and AI systems engineer. Computer Science student at Soongsil University.
I build services end to end: the data model and API, agent orchestration, deployment, observability, and failure recovery.

[Website](https://seongju.vercel.app) · [Email](mailto:seongjuice999@gmail.com) · [한국어](./README_KR.md)

## Experience

- **Founding Engineer, [TrabyOS](https://trabyos-website.vercel.app/)** · Sep 2026 ~ present. The startup's only developer. I build the whole voice-first AI trading workspace alone: Spring Boot core, Python coordinator, Swift native voice client, deterministic instrument resolution, and explicit approval before any order. [GitHub](https://github.com/TrabyOS)
- **Software Engineer Intern, [Bizarre Cube AI](https://www.bzrr.ai/)** ·([MXN Commerce Group](https://www.mxncommerce.com/en)) · Sep 2026 ~ present. Production AI agents for fashion e-commerce operations. [GitHub](https://github.com/bizarrecube)
- **Republic of Korea Army** · May 2023 ~ Nov 2024. Mandatory military service.
- **Soongsil University**, School of Computer Science & Engineering · 2022 ~ present. [Coursework](https://github.com/ghdtjdwn/cs-coursework)

## Projects

- **ssu Campus AI Platform** `Spring Boot` `LangGraph` `Next.js` `Kubernetes`
  Soongsil University's public and personal academic, LMS, and library data, served through a web app, a natural-language agent, and 52 MCP tools. Four services that I designed and operate: [ssuAI](https://github.com/ghdtjdwn/ssuAI) (web, same-origin BFF, SSE), [ssuMCP](https://github.com/ghdtjdwn/ssuMCP) (domain tools, REST, approval-gated writes), [ssuAgent](https://github.com/ghdtjdwn/ssuAgent) (LangGraph routing, PostgreSQL checkpoints, human-in-the-loop), and [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service) (embedding gateway). PostgreSQL is the source of truth, Redis handles coordination and rate limits, Kafka handles fan-out, and Argo CD delivers to ARM64 Kubernetes with Prometheus, Tempo, Loki, and Grafana. [Live](https://ssuai.vercel.app)
- **[Geuneul](https://github.com/ghdtjdwn/geuneul)** `Spring Boot` `PostGIS` `AWS ECS` `Terraform`
  A summer survival map: 150k+ public POIs, radius and kNN search on PostGIS, and real-time user reports over LISTEN/NOTIFY and SSE. Solo project. Terraform-declared AWS, OIDC deploys from GitHub Actions, k6 load tests, and tuning decided from EXPLAIN plans. [Live](https://geuneul.vercel.app)
- **[Cham Domi](https://github.com/chamdormie)** `Spring Boot` `Next.js` `MySQL` `k3s`
  Dormitory discovery with explainable roommate matching and chat, built by a team of three. My part: the frontend, the roommate matching backend (Irving's Stable Roommates checked against a brute-force oracle), chat with MySQL as the authority, and the k3s/Helm production infrastructure. [Live](https://chamdomi.vercel.app)
- **[marketvalley](https://github.com/unithon26/marketvalley)** `Next.js` `Supabase` `Meta Marketing API`
  Automated market validation: one idea in, a landing page, card news, Meta ads, and a real-response report out. My part: backend and AI, the content pipeline, per-user data isolation, long-running jobs, and the Meta Ads integration. [Live](https://marketvaley.vercel.app) · [Team](https://github.com/unithon26)
- **[Folding](https://github.com/dotenv-uploaded/_FOLDING_)** `FastAPI` `Claude Agent SDK` `Electron` `SQLite`
  A local-first document agent that reads, connects, and safely edits HWP, Office, and PDF files while preserving evidence from the originals. Team of four. My part: the entire AI agent runtime and the knowledge graph. The runtime is a FastAPI sidecar built on the Claude Agent SDK where the model gets no write tools, every change is previewed as an exact diff and hash-approved by the user, and files are replaced atomically with crash-recoverable journals and undo. The knowledge graph derives relationships between converted documents from shared entities, keeps the supporting sentence from each source as evidence, and is rebuilt as an immutable version after every verified change. [Team](https://github.com/dotenv-uploaded)
- **[HeungMap](https://github.com/ghdtjdwn/heungmap)** `FastAPI` `LightGBM` `Next.js` `Claude`
  Festival demand forecasting on Korea Tourism Organization open data, entered in the 2026 Tourism Data Contest. Lead developer in a team of two. My part: the D-30 regional visitor model (seasonal baseline plus LightGBM residuals, WAPE 3.9% on a time holdout), the FastAPI service, Claude-written planning reports with server-side checks that reject numbers absent from the input, daily retraining on an Oracle Cloud cron, and the Next.js planner and visitor web app.

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

Java, Kotlin, Spring Boot · Python, FastAPI, LangGraph, MCP · TypeScript, Next.js · PostgreSQL, PostGIS, Redis, Kafka · Docker, Kubernetes, Argo CD, Terraform, AWS · Prometheus, Grafana, Tempo, Loki, OpenTelemetry
