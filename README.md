# Hong Seong Ju

Backend, platform, and AI systems developer at Soongsil University. I focus on systems whose
security boundaries, failure modes, and production behavior can be explained with code and
verification evidence.

[Portfolio](https://seongju.vercel.app/en/) ·
[Email](mailto:seongjuice999@gmail.com) ·
[solved.ac](https://solved.ac/profile/akftjdwn)

## Selected systems

### Soongsil Campus AI Platform

A four-service campus assistant that connects public university data, authenticated u-SAINT and
LMS information, library operations, a web application, and standard MCP clients. The system keeps
browser credentials, agent orchestration, campus-domain tools, and model-serving boundaries in
separate deployable services.

| Service | Responsibility | Link |
| --- | --- | --- |
| ssuAI | Next.js application, same-origin BFF, and streaming chat UX | [Live](https://ssuai.vercel.app) · [Repository](https://github.com/ghdtjdwn/ssuAI) |
| ssuMCP | Spring Boot campus domain server, 52 MCP tools, REST APIs, authentication, and approval-gated writes | [Repository](https://github.com/ghdtjdwn/ssuMCP) |
| ssuAgent | FastAPI and LangGraph routing, PostgreSQL checkpoints, SSE, and human-in-the-loop execution | [Repository](https://github.com/ghdtjdwn/ssuAgent) |
| ssu-ai-service | Independent authenticated Gemini embedding gateway | [Repository](https://github.com/ghdtjdwn/ssu-ai-service) |

The backend uses PostgreSQL as the consistency boundary, Redis for shared coordination and rate
limits, Kafka for durable event fan-out, and Prometheus, Tempo, Loki, and Grafana for operations.
Images are test-gated before GitOps delivery to an ARM64 Kubernetes cluster.

[Architecture and operational evidence](https://seongju.vercel.app/en/projects/ssu-platform/)

### Geuneul

A public summer-survival map for finding shade and heat-relief facilities. PostGIS provides radius,
kNN, and map-bounds search; rerunnable ingestion combines public datasets with persisted geocoding;
Redis protects rate-limited external calls. The product is delivered as a responsive web app, PWA,
and Android package with a Spring Boot backend on AWS ECS Fargate and a Next.js frontend on Vercel.

[Live](https://geuneul.vercel.app) · [Repository](https://github.com/ghdtjdwn/geuneul)

## Engineering focus

- External-system integration with explicit authentication, ownership, retry, and reconciliation
  boundaries.
- PostgreSQL and PostGIS data modeling, idempotent ingestion, background work, caching, and
  concurrency control.
- Production delivery through Docker, Kubernetes, AWS, Terraform, GitHub Actions, ArgoCD, and
  observable runbooks.
- AI features that preserve source provenance, user confirmation, bounded cost, and deterministic
  failure behavior.

## Core stack

Java 21, Kotlin, Spring Boot, Python, FastAPI, LangGraph, Next.js, PostgreSQL, PostGIS, Redis, Kafka,
Docker, Kubernetes, ArgoCD, Terraform, AWS, Prometheus, Tempo, Loki, and Grafana.

## Certifications and problem solving

- 정보처리기능사 (Craftsman Information Processing)
- 컴퓨터활용능력 2급 (Computer Specialist in Spreadsheet & Database Level 2)
- [Baekjoon problem-solving profile](https://solved.ac/profile/akftjdwn)
