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

### marketvalley — UNITHON 2026 Manifest 특별상

예비창업가가 시장 반응을 확인하기 전 반복하던 채널별 기획·제작·광고 등록·데이터 취합을 없애는
자동 시장검증 서비스입니다.

담당 역할: **Backend · AI**

- Zod `CampaignSpec`과 Anthropic Structured Outputs 생성 계약 설계
- Supabase 데이터 모델·RLS, 소유자 API와 공개 랜딩 데이터 경계 구현
- Postgres lease 기반 lifecycle과 Meta 광고·Insights 연동

[서비스](https://marketvaley.vercel.app) ·
[저장소](https://github.com/unithon26/marketvalley) ·
[아키텍처](https://github.com/unithon26/marketvalley/blob/main/docs/architecture.md)

**Cham Domi — 2026학년도 숭실대학교 컴퓨터학부 소프트웨어공모전 은상**

기숙사 탐색부터 설명 가능한 룸메이트 추천, Stable Roommates 자동 배정과 실시간 채팅까지 연결한
3인 팀 서비스입니다. 프론트엔드 전반, roommate 백엔드와 운영 인프라를 맡아 공개 서비스까지
전달했습니다.

[서비스](https://chamdomi.vercel.app) ·
[조직](https://github.com/chamdormie)

## 대표 프로젝트

| 프로젝트 | 직접 맡은 범위 | 원본 · 상세 사례 |
| --- | --- | --- |
| marketvalley | `CampaignSpec`·AI 생성·RLS·장기 실행 상태 머신 | [서비스](https://marketvaley.vercel.app) · [저장소](https://github.com/unithon26/marketvalley) · [아키텍처](https://github.com/unithon26/marketvalley/blob/main/docs/architecture.md) |
| ssu 캠퍼스 AI 플랫폼 | 4개 서비스 설계·구현·운영 | [ssuAI](https://github.com/ghdtjdwn/ssuAI) · [ssuMCP](https://github.com/ghdtjdwn/ssuMCP) · [ssuAgent](https://github.com/ghdtjdwn/ssuAgent) · [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service) · [상세 사례](https://seongju.vercel.app/projects/ssu-platform/) |
| Cham Domi | 프론트엔드·roommate 백엔드·운영 인프라 | [서비스](https://chamdomi.vercel.app) · 비공개 팀 저장소 · [공개 사례](https://seongju.vercel.app/projects/cham-domi/) |
| 그늘 — 여름 생존 지도 | 개인 프로젝트 전체 | [저장소](https://github.com/ghdtjdwn/geuneul) · [상세 사례](https://seongju.vercel.app/projects/geuneul/) |
| UNITHON 음성 키오스크 Macro | 음성 클라이언트·UI 자동화·안전한 주문 인계 | [저장소](https://github.com/UNITHON24/Macro) · [상세 사례](https://seongju.vercel.app/projects/unithon-macro/) |

공개 저장소를 구현 원본으로 먼저 연결하고, 여러 저장소를 묶거나 비공개 팀 저장소인 프로젝트만 공개 사례로 보완했습니다. 팀 프로젝트는 제가 맡은 범위만 적었습니다.

## 최근 만든 시스템: marketvalley

하나의 입력에서 검증 가설, 공개 랜딩, Instagram 카드 5장, 광고 문구와 Meta 광고를 만들고 실제
방문·예약·Insights를 하나의 리포트로 돌려줍니다. 브라우저가 닫히거나 외부 API가 일시 실패해도
Postgres lease 기반 상태 머신이 작업을 이어가며, 계정·예산·종료 시각이 정확히 일치할 때만 광고를
활성화합니다.

```text
SUBMITTED → GENERATING → PREPARING → AWAITING_ACTIVATION
          → COLLECTING → FINALIZING → COMPLETED
```

Next.js 16, TypeScript, Supabase Auth·Postgres·RLS, Anthropic Structured Outputs, Meta Marketing API,
Vercel과 Oracle rootless Docker로 구성했습니다. 생성 결과를 성공처럼 꾸미지 않고 실제 외부 상태와
계측값만 저장·표시하는 경계를 테스트와 운영 문서로 고정했습니다.

[제품 흐름](https://github.com/unithon26/marketvalley#readme) ·
[검증 기록](https://github.com/unithon26/marketvalley/blob/main/docs/validation.md)

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
