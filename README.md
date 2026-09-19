<p align="center">
  <img src="./assets/profile-header.svg" width="100%" alt="Hong Seong Ju — Backend, Platform, and AI Systems" />
</p>

<p align="right"><a href="./README_KR.md">Korean</a></p>

# Hong Seong Ju | Backend · Platform · AI Systems

I study Computer Science at Soongsil University and build and operate backend, data, and AI systems.
I treat authentication boundaries, data consistency, failure recovery, deployment, and observability as
parts of one end-to-end service.

[Email](mailto:seongjuice999@gmail.com)

## Experience

| Role | Period | Work |
| --- | --- | --- |
| Founding Engineer · [TrabyOS](https://trabyos-website.vercel.app/) | Sep 2026 – Present | Building a voice-first AI trading workspace across backend services, agent orchestration, and trading workflows. |
| AI Agent Engineer Intern · [Bizarre Cube AI](https://www.bzrr.ai/) | Sep 2026 – Present | Designing and building production AI agent systems for fashion and e-commerce domain workflows. |

## Open Source Contributions

Merged upstream. Each row links the problem, the fix, and the maintainer review.

| Project | What I fixed | Evidence |
| --- | --- | --- |
| [Ouroboros](https://github.com/Q00/ouroboros) · agent OS and MCP runtime | Cancelling an in-progress `MCPClientAdapter.connect()` left `is_connected=True` and the adapter's own HTTP client open. Reset adapter state and clean up owned resources before re-raising `CancelledError`, with six regression cases. | Reported [#2364](https://github.com/Q00/ouroboros/issues/2364) → merged [PR #2365](https://github.com/Q00/ouroboros/pull/2365), approved by two maintainers |
| [Caveman](https://github.com/JuliusBrussee/caveman) · token-saving skill for coding agents | `--force` never refreshed editor rule files once a repo was initialized, so rule updates could not reach `.cursor`, `.windsurf`, or `.clinerules`. One-character fix with red-first tests. | [PR #1013](https://github.com/JuliusBrussee/caveman/pull/1013) → cherry-picked into [#1015](https://github.com/JuliusBrussee/caveman/pull/1015) and merged with authorship preserved |
| [psycopg](https://github.com/psycopg/psycopg) · PostgreSQL adapter for Python | `AsyncConnectionPool.getconn()` could swallow task cancellation during a connection check, hanging worker shutdown (seen in Procrastinate). Reproduced it, wrote a deterministic check-after-growth regression, and verified the maintainer's fix. | Verification requested and accepted by the maintainer on [#1345](https://github.com/psycopg/psycopg/issues/1345); fixed by [PR #1407](https://github.com/psycopg/psycopg/pull/1407) · [regression tests](https://github.com/MarthalaJagruthiReddy/psycopg/pull/1) |

## Awards

- **Manifest Special Award** · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley) — backend and AI for a marketing-validation tool: Anthropic content pipeline, per-user data isolation, long-running jobs, Meta Ads · [Live](https://marketvaley.vercel.app)
- **Silver Award** · Soongsil CS Software Contest 2026 · [Cham Domi](https://github.com/chamdormie) — frontend, roommate backend, production infrastructure · [Live](https://chamdomi.vercel.app)
- **Excellence Award** · Soongsil Solved Code Algorithm Competition 2025 · [solved.ac](https://solved.ac/profile/akftjdwn)

## SSU Campus AI Platform

An operational platform that connects Soongsil University's public information and personal academic,
LMS, and library data through the web, a natural-language agent, and standard MCP tools. Browser
authentication, conversation orchestration, campus-domain tools, and model serving are separated into
independent service boundaries.

| Service | Responsibility | Links |
| --- | --- | --- |
| ssuAI | Next.js web app, same-origin BFF, responsive dashboards, and SSE/HITL UX | [Service](https://ssuai.vercel.app) · [Repository](https://github.com/ghdtjdwn/ssuAI) |
| ssuMCP | Spring Boot campus domain service, MCP tools, REST APIs, authentication, and approval-gated writes | [Repository](https://github.com/ghdtjdwn/ssuMCP) |
| ssuAgent | FastAPI/LangGraph routing, PostgreSQL checkpoints, SSE, and human-in-the-loop workflows | [Repository](https://github.com/ghdtjdwn/ssuAgent) |
| ssu-ai-service | Standalone embedding gateway with authentication, input, and concurrency boundaries | [Repository](https://github.com/ghdtjdwn/ssu-ai-service) |

PostgreSQL is the source of truth for durable consistency, Redis handles shared coordination and rate
limiting, and Kafka provides event fan-out. Tested images are delivered to ARM64 Kubernetes through
Argo CD, with Prometheus, Tempo, Loki, and Grafana providing operational visibility.

## Technologies and Notes

- Backend · AI: Java 21, Kotlin, Spring Boot, Python, FastAPI, LangGraph, MCP
- Data: PostgreSQL, PostGIS, Redis, Kafka
- Web: TypeScript, Next.js, React, Astro
- Platform: Docker, Kubernetes, Argo CD, Terraform, AWS, GitHub Actions
- Observability: Prometheus, Grafana, Tempo, Loki, OpenTelemetry
- [Computer Science coursework archive](https://github.com/ghdtjdwn/cs-coursework)
