# 홍성주

백엔드·AI 시스템 엔지니어. 숭실대학교 컴퓨터학부 재학 중.
데이터 모델과 API, 에이전트 오케스트레이션, 배포, 관측, 장애 복구까지 서비스를 끝까지 만들고 운영합니다.

[이메일](mailto:seongjuice999@gmail.com) · [English](./README.md)

## 경력

- **Founding Engineer, [TrabyOS](https://github.com/TrabyOS)** · 2026.09 ~ 현재. 결정적 주문 해석부터 macOS 네이티브 음성 인터페이스까지 음성 중심 AI 트레이딩 워크스페이스의 기술을 총괄. [웹사이트](https://trabyos-website.vercel.app/) · [무료 테스트 빌드](https://github.com/TrabyOS/trabyos-test/releases/latest)
- **Software Engineer Intern, [비자르큐브 AI](https://www.bzrr.ai/)** · [MXN Commerce Group](https://www.mxncommerce.com/en) · 2026.09 ~ 현재. 패션 이커머스 운영 업무를 위한 실서비스 AI 에이전트.
- **대한민국 육군** · 2023.05 ~ 2024.11. 병역 이행.
- **숭실대학교 컴퓨터학부** · 2022 ~ 현재.

## 프로젝트

- **ssu 캠퍼스 AI 플랫폼** `Spring Boot` `LangGraph` `Next.js` `Kubernetes`
  숭실대학교의 공개 정보와 개인 학사·LMS·도서관 데이터를 웹, 자연어 에이전트, 승인 경계를 갖춘 52개 MCP 도구로 제공합니다. [ssuAI](https://github.com/ghdtjdwn/ssuAI), [ssuMCP](https://github.com/ghdtjdwn/ssuMCP), [ssuAgent](https://github.com/ghdtjdwn/ssuAgent), [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service)로 나눠 ARM64 Kubernetes에 배포하고 전 구간을 관측합니다. [웹](https://ssuai.vercel.app)
- **[그늘](https://github.com/ghdtjdwn/geuneul)** `Spring Boot` `PostGIS` `AWS → OCI` `Terraform`
  공공 POI 15만 건 이상을 GiST 기반 반경·kNN으로 검색하고 LISTEN/NOTIFY와 SSE로 실시간 제보를 전달하는 여름 생존 지도입니다. 저장소에 AWS에서 OCI로 데이터를 보존하며 이전하는 현재 상태를 기록합니다. [웹](https://geuneul.vercel.app)
- **[참도미](https://github.com/chamdormie)** `Spring Boot` `Next.js` `MySQL` `k3s`
  기숙사 탐색, 설명 가능한 룸메이트 매칭, 채팅을 잇습니다. 매칭 엔진은 Irving의 Stable Roommates 알고리즘을 구현하고 완전 탐색 오라클과 대조해 검증했습니다. [웹](https://chamdomi.vercel.app)
- **[marketvalley](https://github.com/unithon26/marketvalley)** `Next.js` `Supabase` `Meta Marketing API`
  아이디어 하나를 랜딩, 소셜 카드 5장, Meta 광고, 실제 방문·예약·Insights에 근거한 리포트로 이어 줍니다. 브라우저를 닫아도 PostgreSQL lease 상태 머신이 장기 작업을 계속합니다. [웹](https://marketvaley.vercel.app)
- **[Folding](https://github.com/dotenv-uploaded/_FOLDING_)** `FastAPI` `Gemma 4` `Electron` `SQLite`
  HWP·Office·PDF를 다루는 로컬 우선 문서 에이전트입니다. 원문 근거를 보존하는 지식 그래프로 문서를 연결하고, exact diff 승인·원본 해시 검증·원자적 교체·undo로 수정을 검토 가능하고 복구 가능하게 만듭니다.
- **[흥할지도](https://github.com/ghdtjdwn/heungmap)** `FastAPI` `LightGBM` `Next.js` `Claude`
  한국관광공사 공개 데이터로 축제 수요를 예측합니다. 계절 기준선에 LightGBM 잔차 모델을 더해 시간 홀드아웃 WAPE 3.9%를 기록했고, 생성된 기획 보고서의 숫자가 모델 입력에 없으면 서버가 거부합니다.

## 오픈소스

업스트림에 병합된 기여입니다. [전체 PR 보기](https://github.com/search?q=is%3Apr+author%3Aghdtjdwn+-org%3Aghdtjdwn&type=pullrequests)

- **[psycopg](https://github.com/psycopg/psycopg)** `Python` · `AsyncConnectionPool.getconn()`이 연결 검사 도중 태스크 취소를 삼켜 워커 종료가 멈추는 문제. 재현하고 결정적 회귀 테스트를 작성해 유지보수자의 수정을 검증. [#1345](https://github.com/psycopg/psycopg/issues/1345) · [PR #1407](https://github.com/psycopg/psycopg/pull/1407)
- **[Ouroboros](https://github.com/Q00/ouroboros)** `Python` · 진행 중인 MCP 클라이언트 연결이 취소되면 어댑터가 연결 상태로 남고 HTTP 클라이언트가 열린 채 유지되는 문제. 다시 던지기 전에 상태를 초기화하고 소유 자원을 정리, 회귀 테스트 6건. [#2364](https://github.com/Q00/ouroboros/issues/2364) · [PR #2365](https://github.com/Q00/ouroboros/pull/2365)
- **[Caveman](https://github.com/JuliusBrussee/caveman)** `Go` · 한 번 초기화된 저장소에서 `--force`로도 에디터 규칙 파일이 갱신되지 않던 문제. 한 글자 수정과 실패 우선 테스트. [PR #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · [#1015](https://github.com/JuliusBrussee/caveman/pull/1015)로 병합

리뷰 진행 중: [Micrometer](https://github.com/micrometer-metrics/micrometer/pull/7925), [OpenTelemetry Python Contrib](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032), [Spring AI](https://github.com/spring-projects/spring-ai/pull/6929), [Lettuce](https://github.com/redis/lettuce/pull/3909), [SlowAPI](https://github.com/laurentS/slowapi/pull/305).


## 수상

- 🏆 매니패스트 특별상 · UNITHON 2026 · marketvalley
- 🥈 은상 · 숭실대학교 컴퓨터학부 소프트웨어공모전 2026 · 참도미
- 🏅 우수상 · 숭실대학교 솔브드 코드 알고리즘 대회 2025

## 기술

Java, Kotlin, Spring Boot · Python, FastAPI, LangGraph, MCP · TypeScript, Next.js · Swift, macOS · PostgreSQL, PostGIS, Redis, Kafka · Docker, Kubernetes, Argo CD, Terraform, AWS, OCI · Prometheus, Grafana, Tempo, Loki, OpenTelemetry
