<p align="center">
  <img src="./assets/profile-header.svg" width="100%" alt="Hong Seong Ju — Backend, Platform, and AI Systems" />
</p>

<p align="right"><a href="./README_KR.md">Korean</a></p>

# Hong Seong Ju | Backend · Platform · AI Systems

I study Computer Science at Soongsil University and build and operate backend, data, and AI systems.
I treat authentication boundaries, data consistency, failure recovery, deployment, and observability as
parts of one end-to-end service.

[Technical Blog](https://seongju.vercel.app/en/) ·
[Blog (Korean)](https://seongju.vercel.app) ·
[Email](mailto:seongjuice999@gmail.com)

## Experience

| Role | Period | Focus |
| --- | --- | --- |
| Founding Engineer · [TrabyOS](https://trabyos-website.vercel.app/) | Sep 2026 – Present | Building a voice-first AI trading workspace across backend services, agent orchestration, and trading workflows. |
| AI Agent Engineer Intern · [Bizarre Cube AI](https://www.bzrr.ai/) | Sep 2026 – Present | Designing and building production AI agent systems for fashion and e-commerce businesses. |

## Recent Awards

| Award | Scope | Outcome · Evidence |
| --- | --- | --- |
| UNITHON 2026 — Manifest Special Award · marketvalley | Backend & AI: data flows connecting validation hypotheses to landing pages, social media cards, and ad copy; Anthropic-powered generation; per-user data isolation and APIs; long-running job state management; Meta Ads and Insights | Official Manifest Special Award · [Service](https://marketvaley.vercel.app) · [Repository](https://github.com/unithon26/marketvalley) |
| 2026 Soongsil University School of Computer Science Software Contest — Silver Award · Cham Domi | End-to-end frontend, roommate backend, and production infrastructure | Silver Award and public service delivery · [Service](https://chamdomi.vercel.app) · [Organization](https://github.com/chamdormie) |
| Soongsil University Solved Code Algorithm Competition — Excellence Award · 2025 | Problem analysis, algorithm design, and implementation | Excellence Award · [solved.ac](https://solved.ac/profile/akftjdwn) |

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

[Architecture and operations notes](https://seongju.vercel.app/en/projects/ssu-platform/)

## Technologies and Notes

- Backend · AI: Java 21, Kotlin, Spring Boot, Python, FastAPI, LangGraph, MCP
- Data: PostgreSQL, PostGIS, Redis, Kafka
- Web: TypeScript, Next.js, React, Astro
- Platform: Docker, Kubernetes, Argo CD, Terraform, AWS, GitHub Actions
- Observability: Prometheus, Grafana, Tempo, Loki, OpenTelemetry
- [Computer Science coursework archive](https://github.com/ghdtjdwn/cs-coursework)
