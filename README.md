<p align="center">
  <img src="./assets/profile-header.svg" width="100%" alt="Hong Seong Ju — Backend, Platform, and AI Systems" />
</p>

# 홍성주 | Backend · Platform · AI Systems

숭실대학교 컴퓨터학부에서 사용자 흐름을 끝까지 책임지는 백엔드·플랫폼 엔지니어를 지향합니다.
기능 구현에 그치지 않고 인증 경계, 데이터 정합성, 장애 복구, 배포와 관측까지 설명할 수 있는
시스템을 만듭니다.

[포트폴리오](https://seongju.vercel.app) ·
[English portfolio](https://seongju.vercel.app/en/) ·
[Email](mailto:seongjuice999@gmail.com) ·
[solved.ac](https://solved.ac/profile/akftjdwn)

## 최근 수상

| 수상 | 맡은 범위 | 핵심 성과 · 근거 |
| --- | --- | --- |
| UNITHON 2026 공식 수상 — 매니패스트 특별상 · marketvalley | Backend·AI: 검증 가설부터 랜딩·카드뉴스·광고 문구까지 잇는 데이터 구조, Anthropic 생성, 사용자별 데이터 격리·API, 장기 실행 상태 관리, Meta 광고·Insights | 매니패스트 특별상 공식 수상 · [서비스](https://marketvaley.vercel.app) · [저장소](https://github.com/unithon26/marketvalley) |
| 2026학년도 숭실대학교 컴퓨터학부 소프트웨어공모전 은상 — Cham Domi | 프론트엔드 전반, roommate 백엔드, 운영 인프라 | 은상 수상과 공개 서비스 전달 · [서비스](https://chamdomi.vercel.app) · [조직](https://github.com/chamdormie) |
| 숭실대학교 알고리즘 솔브드 코드 대회 우수상 — 2025 | 대회 문제 분석·알고리즘 설계·구현 | 우수상 수상 · [solved.ac](https://solved.ac/profile/akftjdwn) |

## 대표 프로젝트

| 프로젝트 | 맡은 범위 | 핵심 성과 · 근거 |
| --- | --- | --- |
| marketvalley | 랜딩·카드뉴스·광고 문구를 잇는 데이터 구조, AI 생성, 사용자별 데이터 격리·API, 장기 실행 상태 관리 | UNITHON 2026 매니패스트 특별상 공식 수상, 실제 Meta 광고·Insights 연결 · [서비스](https://marketvaley.vercel.app) · [저장소](https://github.com/unithon26/marketvalley) |
| ssu 캠퍼스 AI 플랫폼 | 4개 서비스 설계·구현·운영 | 52개 MCP 도구와 ARM64 Kubernetes 운영·관측 · [저장소](https://github.com/ghdtjdwn/ssuMCP) · [상세 사례](https://seongju.vercel.app/projects/ssu-platform/) |
| Cham Domi | 프론트엔드·roommate 백엔드·운영 인프라 | 소프트웨어공모전 은상, 공개 서비스 전달 · [서비스](https://chamdomi.vercel.app) · [공개 사례](https://seongju.vercel.app/projects/cham-domi/) |
| 그늘 — 여름 생존 지도 | 개인 프로젝트 전체 | 15만 건 이상 공공 POI ETL·PostGIS 공간 검색·AWS 운영 · [저장소](https://github.com/ghdtjdwn/geuneul) · [상세 사례](https://seongju.vercel.app/projects/geuneul/) |
| UNITHON 음성 키오스크 Macro | 음성 클라이언트·semantic UI 자동화·안전한 주문 인계 | 좌표 의존을 줄인 자동화와 Ubuntu·Windows 안전 코어 테스트 69개 · [저장소](https://github.com/UNITHON24/Macro) · [상세 사례](https://seongju.vercel.app/projects/unithon-macro/) |

공개 저장소를 구현 원본으로 먼저 연결하고, 여러 저장소를 묶거나 비공개 팀 저장소인 프로젝트만 공개 사례로 보완했습니다. 팀 프로젝트는 제가 맡은 범위만 적었습니다.

## 대표 시스템: ssu 캠퍼스 AI 플랫폼

숭실대학교의 공개 정보와 개인 학사·LMS·도서관 데이터를 웹, 자연어 에이전트와 표준 MCP 도구로
연결한 운영형 플랫폼입니다. 브라우저 인증, 대화 오케스트레이션, 캠퍼스 도메인 도구와 모델 서빙을
각각 독립된 서비스 경계로 분리했습니다.

| 서비스 | 책임 | 확인 |
| --- | --- | --- |
| ssuAI | Next.js 웹, same-origin BFF, 반응형 대시보드와 SSE/HITL UX | [서비스](https://ssuai.vercel.app) · [저장소](https://github.com/ghdtjdwn/ssuAI) |
| ssuMCP | Spring Boot 캠퍼스 도메인, 52개 MCP 도구, REST, 인증과 승인 기반 쓰기 | [저장소](https://github.com/ghdtjdwn/ssuMCP) |
| ssuAgent | FastAPI/LangGraph 라우팅, PostgreSQL checkpoint, SSE와 human-in-the-loop | [저장소](https://github.com/ghdtjdwn/ssuAgent) |
| ssu-ai-service | 인증·입력·동시성 경계를 둔 독립 임베딩 게이트웨이 | [저장소](https://github.com/ghdtjdwn/ssu-ai-service) |

PostgreSQL을 영속 정합성의 기준으로 두고 Redis로 공유 조정과 rate limit을, Kafka로 이벤트 fan-out을
처리합니다. 테스트를 통과한 이미지를 ArgoCD로 ARM64 Kubernetes에 전달하며 Prometheus, Tempo, Loki와
Grafana로 운영 상태를 확인합니다.

[아키텍처·운영 근거가 포함된 사례 읽기](https://seongju.vercel.app/projects/ssu-platform/)

## 주로 사용하는 기술

| 영역 | 기술 |
| --- | --- |
| Backend · AI | Java 21, Kotlin, Spring Boot, Python, FastAPI, LangGraph, MCP |
| Data | PostgreSQL, PostGIS, Redis, Kafka |
| Web | TypeScript, Next.js, React, Astro |
| Platform | Docker, Kubernetes, ArgoCD, Terraform, AWS, GitHub Actions |
| Observability | Prometheus, Grafana, Tempo, Loki, OpenTelemetry |

## 학습 기록과 자격

- [컴퓨터학부 전공 과제 아카이브](https://github.com/ghdtjdwn/cs-coursework): 시스템, 알고리즘, 네트워크, AI와 데이터 분석
- 정보처리기능사 (Craftsman Information Processing)
- 컴퓨터활용능력 2급 (Computer Specialist in Spreadsheet & Database Level 2)
