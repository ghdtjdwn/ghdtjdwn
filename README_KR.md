<p align="center">
  <img src="./assets/profile-header.svg" width="100%" alt="홍성주 — Backend, Platform, and AI Systems" />
</p>

<p align="right"><a href="./README.md">English</a></p>

# 홍성주 | Backend · Platform · AI Systems

숭실대학교 컴퓨터학부에서 공부하며 백엔드, 데이터와 AI 시스템을 만들고 운영합니다.
인증 경계, 데이터 정합성, 장애 복구, 배포와 관측을 하나의 서비스 흐름으로 다룹니다.

[Email](mailto:seongjuice999@gmail.com)

## 경력

| 역할 | 기간 | 주요 업무 |
| --- | --- | --- |
| Founding Engineer · [TrabyOS](https://trabyos-website.vercel.app/) | 2026.09 – 현재 | 백엔드 서비스, 에이전트 오케스트레이션과 트레이딩 워크플로 전반에서 음성 중심 AI 트레이딩 워크스페이스를 개발합니다. |
| AI Agent Engineer Intern · [Bizarre Cube AI](https://www.bzrr.ai/) | 2026.09 – 현재 | 패션·이커머스 기업의 도메인 업무를 위한 AI 에이전트 시스템을 실서비스 환경에 맞게 설계하고 개발합니다. |

## 오픈소스 기여

업스트림에 병합된 기여입니다. 각 행에 문제, 수정, 유지보수자 리뷰를 함께 연결했습니다.

| 프로젝트 | 해결한 문제 | 근거 |
| --- | --- | --- |
| [Ouroboros](https://github.com/Q00/ouroboros) · 에이전트 OS·MCP 런타임 | 진행 중인 `MCPClientAdapter.connect()`가 취소되면 `is_connected=True`와 어댑터 소유 HTTP 클라이언트가 열린 채 남는 문제. `CancelledError`를 다시 던지기 전에 어댑터 상태를 초기화하고 소유 자원을 정리하도록 수정, 회귀 테스트 6건 추가 | [#2364](https://github.com/Q00/ouroboros/issues/2364) 보고 → [PR #2365](https://github.com/Q00/ouroboros/pull/2365) 병합, 유지보수자 2명 승인 |
| [Caveman](https://github.com/JuliusBrussee/caveman) · 코딩 에이전트 토큰 절감 스킬 | 한 번 초기화된 저장소에서는 `--force`로도 에디터 규칙 파일이 갱신되지 않아 `.cursor`·`.windsurf`·`.clinerules`에 규칙 변경이 전달되지 않던 문제. 한 글자 수정과 실패 우선 테스트 | [PR #1013](https://github.com/JuliusBrussee/caveman/pull/1013) → [#1015](https://github.com/JuliusBrussee/caveman/pull/1015)에 cherry-pick되어 작성자 이력 보존 후 병합 |
| [psycopg](https://github.com/psycopg/psycopg) · Python PostgreSQL 어댑터 | `AsyncConnectionPool.getconn()`이 연결 검사 도중 태스크 취소를 잃어 워커 종료가 멈추는 문제(Procrastinate에서 발생). 재현하고 결정적 회귀 테스트(풀 확장 후 검사 취소)를 작성해 유지보수자 수정을 검증 | 유지보수자가 [#1345](https://github.com/psycopg/psycopg/issues/1345)에서 검증을 요청·수용, [PR #1407](https://github.com/psycopg/psycopg/pull/1407)로 수정 확정 · [회귀 테스트](https://github.com/MarthalaJagruthiReddy/psycopg/pull/1) |

## 최근 수상

| 수상 | 맡은 범위 | 핵심 성과 · 근거 |
| --- | --- | --- |
| UNITHON 2026 공식 수상 — 매니패스트 특별상 · marketvalley | Backend·AI: 검증 가설부터 랜딩·카드뉴스·광고 문구까지 잇는 데이터 구조, Anthropic 생성, 사용자별 데이터 격리·API, 장기 실행 상태 관리, Meta 광고·Insights | 매니패스트 특별상 공식 수상 · [서비스](https://marketvaley.vercel.app) · [저장소](https://github.com/unithon26/marketvalley) |
| 2026학년도 숭실대학교 컴퓨터학부 소프트웨어공모전 은상 — Cham Domi | 프론트엔드 전반, roommate 백엔드, 운영 인프라 | 은상 수상과 공개 서비스 전달 · [서비스](https://chamdomi.vercel.app) · [조직](https://github.com/chamdormie) |
| 숭실대학교 알고리즘 솔브드 코드 대회 우수상 — 2025 | 대회 문제 분석·알고리즘 설계·구현 | 우수상 수상 · [solved.ac](https://solved.ac/profile/akftjdwn) |

## ssu 캠퍼스 AI 플랫폼

숭실대학교의 공개 정보와 개인 학사·LMS·도서관 데이터를 웹, 자연어 에이전트와 표준 MCP 도구로
연결한 운영형 플랫폼입니다. 브라우저 인증, 대화 오케스트레이션, 캠퍼스 도메인 도구와 모델 서빙을
각각 독립된 서비스 경계로 분리했습니다.

| 서비스 | 책임 | 링크 |
| --- | --- | --- |
| ssuAI | Next.js 웹, same-origin BFF, 반응형 대시보드와 SSE/HITL UX | [서비스](https://ssuai.vercel.app) · [저장소](https://github.com/ghdtjdwn/ssuAI) |
| ssuMCP | Spring Boot 캠퍼스 도메인, MCP 도구, REST, 인증과 승인 기반 쓰기 | [저장소](https://github.com/ghdtjdwn/ssuMCP) |
| ssuAgent | FastAPI/LangGraph 라우팅, PostgreSQL checkpoint, SSE와 human-in-the-loop | [저장소](https://github.com/ghdtjdwn/ssuAgent) |
| ssu-ai-service | 인증·입력·동시성 경계를 둔 독립 임베딩 게이트웨이 | [저장소](https://github.com/ghdtjdwn/ssu-ai-service) |

PostgreSQL을 영속 정합성의 기준으로 두고 Redis로 공유 조정과 rate limit을, Kafka로 이벤트 fan-out을
처리합니다. 테스트를 통과한 이미지를 Argo CD로 ARM64 Kubernetes에 전달하며 Prometheus, Tempo, Loki와
Grafana로 운영 상태를 확인합니다.

## 기술과 기록

- Backend · AI: Java 21, Kotlin, Spring Boot, Python, FastAPI, LangGraph, MCP
- Data: PostgreSQL, PostGIS, Redis, Kafka
- Web: TypeScript, Next.js, React, Astro
- Platform: Docker, Kubernetes, Argo CD, Terraform, AWS, GitHub Actions
- Observability: Prometheus, Grafana, Tempo, Loki, OpenTelemetry
- [컴퓨터학부 전공 과제 아카이브](https://github.com/ghdtjdwn/cs-coursework)
