# 홍성주 | Backend · Platform · AI Systems

숭실대학교 컴퓨터학부에서 백엔드와 플랫폼을 공부하고 있습니다. 기능 구현에 그치지 않고
인증 경계, 데이터 정합성, 장애 복구, 배포와 관측까지 설명할 수 있는 시스템을 만듭니다.

[포트폴리오](https://seongju.vercel.app) ·
[English portfolio](https://seongju.vercel.app/en/) ·
[Email](mailto:seongjuice999@gmail.com) ·
[solved.ac](https://solved.ac/profile/akftjdwn)

## 대표 프로젝트

| 프로젝트 | 직접 맡은 범위 | 핵심 구현과 근거 |
| --- | --- | --- |
| [ssu 캠퍼스 AI 플랫폼](https://seongju.vercel.app/projects/ssu-platform/) | 4개 서비스 설계·구현·운영 | Spring Boot MCP/REST, LangGraph, Next.js, PostgreSQL·Redis·Kafka, ARM64 k3s GitOps |
| [그늘 — 여름 생존 지도](https://github.com/ghdtjdwn/geuneul) | 개인 프로젝트 전체 | 15만여 공공 POI, PostGIS 공간 검색, 재실행 가능한 ETL, AWS ECS Fargate·Terraform |
| [UNITHON 음성 키오스크 Macro](https://github.com/UNITHON24/Macro) | 음성 클라이언트·UI 자동화·안전한 주문 인계 | Windows UIA 우선 탐색, OCR fallback, 영속 주문 큐, 결제 입력 전 정지 |
| [Cham Domi](https://seongju.vercel.app/projects/cham-domi/) | 프론트엔드 전체·roommate 백엔드 | Next.js 화면 흐름, Spring Boot/JPA, Stable Roommates와 FE/BE parity test |

팀 프로젝트는 제가 맡은 범위만 적었고, 비공개 저장소는 공개 사례의 검증 가능한 설명으로 연결했습니다.

## Flagship: ssu 캠퍼스 AI 플랫폼

숭실대학교의 공개 정보와 개인 학사·LMS·도서관 데이터를 웹, 자연어 에이전트와 표준 MCP 도구로
연결한 운영형 플랫폼입니다. 브라우저 인증, 대화 오케스트레이션, 캠퍼스 도메인 도구와 모델 서빙을
각각 독립된 서비스 경계로 분리했습니다.

| 서비스 | 책임 | 확인 |
| --- | --- | --- |
| ssuAI | Next.js 웹, same-origin BFF, 반응형 대시보드와 SSE/HITL UX | [Live](https://ssuai.vercel.app) · [Repository](https://github.com/ghdtjdwn/ssuAI) |
| ssuMCP | Spring Boot 캠퍼스 도메인, 52개 MCP 도구, REST, 인증과 승인 기반 쓰기 | [Repository](https://github.com/ghdtjdwn/ssuMCP) |
| ssuAgent | FastAPI/LangGraph 라우팅, PostgreSQL checkpoint, SSE와 human-in-the-loop | [Repository](https://github.com/ghdtjdwn/ssuAgent) |
| ssu-ai-service | 인증·입력·동시성 경계를 둔 독립 임베딩 게이트웨이 | [Repository](https://github.com/ghdtjdwn/ssu-ai-service) |

PostgreSQL을 영속 정합성의 기준으로 두고 Redis로 공유 조정과 rate limit을, Kafka로 이벤트 fan-out을
처리합니다. 테스트를 통과한 이미지를 ArgoCD로 ARM64 Kubernetes에 전달하며 Prometheus, Tempo, Loki와
Grafana로 운영 상태를 확인합니다.

[아키텍처·운영 근거가 포함된 사례 읽기](https://seongju.vercel.app/projects/ssu-platform/)

## 만드는 방식

- 외부 시스템은 connector와 명시적 timeout·fallback·reconciliation 경계 뒤에 둡니다.
- 상태 변경은 소유권을 검증하고 `prepare → confirm`으로 나눠 사용자 승인 전에는 실행하지 않습니다.
- 성능 수치는 실행계획과 제한된 부하 조건을 함께 기록하고, 검증 범위를 결과보다 넓게 주장하지 않습니다.
- 작업 로그, ADR, troubleshooting, 테스트와 배포 증거를 남겨 선택과 실패를 다시 설명할 수 있게 합니다.

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
