# 홍성주

백엔드·AI 시스템 엔지니어. 숭실대학교 컴퓨터학부 재학 중.
데이터 모델과 API, 에이전트 오케스트레이션, 배포, 관측, 장애 복구까지 서비스를 끝까지 만들고 운영합니다.

[웹사이트](https://seongju.vercel.app) · [이메일](mailto:seongjuice999@gmail.com) · [English](./README.md)

## 경력

- **Founding Engineer, [TrabyOS](https://trabyos-website.vercel.app/)** · 2026.09 ~ 현재. 이 스타트업의 유일한 개발자로 음성 중심 AI 트레이딩 워크스페이스 전체를 혼자 개발. Spring Boot 코어, Python 코디네이터, Swift 네이티브 음성 클라이언트, 결정적 종목 해석, 주문 전 명시적 승인. [GitHub](https://github.com/TrabyOS)
- **Software Engineer Intern, [비자르큐브 AI](https://www.bzrr.ai/)** · [MXN Commerce Group](https://www.mxncommerce.com/en) · 2026.09 ~ 현재. 패션 이커머스 운영 업무를 위한 실서비스 AI 에이전트. [GitHub](https://github.com/bizarrecube)
- **대한민국 육군** · 2023.05 ~ 2024.11. 병역 이행.
- **숭실대학교 컴퓨터학부** · 2022 ~ 현재. [전공 과제 아카이브](https://github.com/ghdtjdwn/cs-coursework)

## 프로젝트

- **ssu 캠퍼스 AI 플랫폼** `Spring Boot` `LangGraph` `Next.js` `Kubernetes`
  숭실대학교의 공개 정보와 개인 학사·LMS·도서관 데이터를 웹, 자연어 에이전트, 52개 MCP 도구로 제공합니다. 직접 설계하고 운영하는 4개 서비스: [ssuAI](https://github.com/ghdtjdwn/ssuAI)(웹, same-origin BFF, SSE), [ssuMCP](https://github.com/ghdtjdwn/ssuMCP)(도메인 도구, REST, 승인 기반 쓰기), [ssuAgent](https://github.com/ghdtjdwn/ssuAgent)(LangGraph 라우팅, PostgreSQL checkpoint, human-in-the-loop), [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service)(임베딩 게이트웨이). PostgreSQL을 정본으로 두고 Redis로 조정과 rate limit을, Kafka로 fan-out을 처리하며 Argo CD로 ARM64 Kubernetes에 배포하고 Prometheus·Tempo·Loki·Grafana로 관측합니다. [서비스](https://ssuai.vercel.app)
- **[그늘](https://github.com/ghdtjdwn/geuneul)** `Spring Boot` `PostGIS` `AWS ECS` `Terraform`
  여름 생존 지도. 공공 POI 15만 건 이상, PostGIS 반경·kNN 검색, LISTEN/NOTIFY와 SSE로 전달하는 실시간 제보. 1인 프로젝트. Terraform으로 선언한 AWS, GitHub Actions OIDC 배포, k6 부하 테스트, EXPLAIN 계획에 근거한 튜닝. [서비스](https://geuneul.vercel.app)
- **[참도미](https://github.com/chamdormie)** `Spring Boot` `Next.js` `MySQL` `k3s`
  기숙사 탐색과 설명 가능한 룸메이트 매칭, 채팅. 3인 팀. 담당: 프론트엔드, 룸메이트 매칭 백엔드(Irving의 Stable Roommates를 완전 탐색 오라클과 대조 검증), MySQL을 정본으로 하는 채팅, k3s/Helm 운영 인프라. [서비스](https://chamdomi.vercel.app)
- **[marketvalley](https://github.com/unithon26/marketvalley)** `Next.js` `Supabase` `Meta Marketing API`
  자동 시장 검증. 아이디어 한 번 입력으로 랜딩, 카드뉴스, Meta 광고, 실제 반응 리포트까지. 담당: 백엔드와 AI, 콘텐츠 생성 파이프라인, 사용자별 데이터 격리, 장기 실행 작업, Meta 광고 연동. [서비스](https://marketvaley.vercel.app) · [팀](https://github.com/unithon26)
- **[Folding](https://github.com/dotenv-uploaded/_FOLDING_)** `FastAPI` `Claude Agent SDK` `Electron` `SQLite`
  HWP·Office·PDF 문서를 읽고 연결하고 원본 근거를 보존한 채 안전하게 수정하는 로컬 우선 문서 에이전트. 4인 팀. 담당: AI 에이전트 런타임 전체와 지식 그래프 구축. 런타임은 Claude Agent SDK 기반 FastAPI 사이드카로 모델에는 쓰기 도구를 주지 않고, 모든 변경을 exact diff로 미리 보여 준 뒤 사용자가 해시를 승인해야만 실행하며, 저널과 undo를 갖춘 원자적 파일 교체를 수행. 지식 그래프는 변환된 문서들이 공유하는 엔티티로 관계를 도출하고, 각 원문의 근거 문장을 함께 보존하며, 검증된 변경마다 불변 버전으로 다시 빌드. [팀](https://github.com/dotenv-uploaded)
- **[흥할지도](https://github.com/ghdtjdwn/heungmap)** `FastAPI` `LightGBM` `Next.js` `Claude`
  한국관광공사 공개 데이터로 축제 수요를 예측하는 2026 관광데이터 활용 공모전 출품작. 2인 팀 주 개발자. 담당: D-30 지역 방문수요 모델(계절 기준선 + LightGBM 잔차 보정, 시간 홀드아웃 WAPE 3.9%), FastAPI 서비스, 입력에 없는 숫자를 서버가 검사해 거부하는 Claude 기획 보고서, 오라클 클라우드 cron 일일 재학습, Next.js 기획자·방문객 웹.

## 오픈소스

주로 동시 실행 런타임에서의 취소, 경쟁 상태, 유실되는 상태를 다루며, 모두 재현과 실패하는 테스트에서 출발했습니다. [전체 PR 보기](https://github.com/search?q=is%3Apr+author%3Aghdtjdwn+-org%3Aghdtjdwn&type=pullrequests)

**업스트림 병합**

- **[psycopg](https://github.com/psycopg/psycopg)** `Python` · `AsyncConnectionPool.getconn()`이 연결 검사 도중 태스크 취소를 삼켜 워커 종료가 멈추는 문제. 재현하고 결정적 회귀 테스트를 작성해 유지보수자의 수정을 검증. [#1345](https://github.com/psycopg/psycopg/issues/1345) · [PR #1407](https://github.com/psycopg/psycopg/pull/1407)
- **[Ouroboros](https://github.com/Q00/ouroboros)** `Python` · 진행 중인 MCP 클라이언트 연결이 취소되면 어댑터가 연결 상태로 남고 HTTP 클라이언트가 열린 채 유지되는 문제. 다시 던지기 전에 상태를 초기화하고 소유 자원을 정리, 회귀 테스트 6건. [#2364](https://github.com/Q00/ouroboros/issues/2364) · [PR #2365](https://github.com/Q00/ouroboros/pull/2365)
- **[Caveman](https://github.com/JuliusBrussee/caveman)** `Go` · 한 번 초기화된 저장소에서 `--force`로도 에디터 규칙 파일이 갱신되지 않던 문제. 한 글자 수정과 실패 우선 테스트. [PR #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · [#1015](https://github.com/JuliusBrussee/caveman/pull/1015)로 병합

**리뷰 진행 중**

- **[OpenTelemetry Python](https://github.com/open-telemetry/opentelemetry-python-contrib)** `Python` · WSGI SERVER 스팬이 캡처한 요청 헤더를 샘플링 이후에 설정해 샘플러가 헤더를 볼 수 없던 문제. 설정된 헤더를 정제해 스팬 초기 속성으로 전달하고 INTERNAL 스팬과 메트릭에는 포함하지 않도록 유지. 리뷰에서 요청받은 공통 `CapturingSampler` 테스트 유틸리티는 core 저장소에 추가. [contrib PR #5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032) · [core PR #5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681)
- **[Lettuce](https://github.com/redis/lettuce)** `Java` · 연결 초기화 중 동시 `setOptions()` 호출이 설정을 섞을 수 있는 문제. 캡처한 `ClientOptions`를 `RedisClient`, `RedisClusterClient`, 공유 핸드셰이크에 전달(커스텀 팩토리 훅과 비동기 재시도 포함). 유지보수자가 공개 연결 팩토리 API에 `ClientOptions` 파라미터를 명시적으로 추가하는 방향으로 확장을 제안. [#3591](https://github.com/redis/lettuce/issues/3591) · [PR #3909](https://github.com/redis/lettuce/pull/3909)
- **[Spring AI](https://github.com/spring-projects/spring-ai)** `Java` · `RedisChatMemoryRepository`에 의존하는 커스텀 `ChatMemory` 빈이 리포지토리 자동 설정을 막아 컨텍스트 기동이 실패하던 문제. 누락 빈 조건을 `ChatMemoryRepository`로 한정하고 커스텀 메모리, 커스텀 리포지토리 우선순위, 기본 메모리에 대한 통합 테스트 추가. [#6926](https://github.com/spring-projects/spring-ai/issues/6926) · [PR #6929](https://github.com/spring-projects/spring-ai/pull/6929)
- **[SlowAPI](https://github.com/laurentS/slowapi)** `Python` · 엔드포인트를 모듈과 `__name__`으로 식별해 `First.index`와 `Second.index` 같은 동명 클래스 메서드가 rate limit과 예외 설정을 공유하던 문제. 등록, 조회, 예외, 미들웨어 매칭 모두 `__qualname__`을 사용하도록 통일, 회귀 테스트 18건. [#173](https://github.com/laurentS/slowapi/issues/173) · [PR #305](https://github.com/laurentS/slowapi/pull/305)
- **[Micrometer](https://github.com/micrometer-metrics/micrometer)** `Java` · Java `HttpClient` observation의 커스텀 태그를 `HttpClientObservationConvention`으로 설정하는 방법을 컴파일되는 테스트 예제로 문서화. [#4962](https://github.com/micrometer-metrics/micrometer/issues/4962) · [PR #7925](https://github.com/micrometer-metrics/micrometer/pull/7925)

## 수상

- 🏆 매니패스트 특별상 · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 은상 · 숭실대학교 컴퓨터학부 소프트웨어공모전 2026 · [참도미](https://github.com/chamdormie)
- 🏅 우수상 · 숭실대학교 솔브드 코드 알고리즘 대회 2025

## 기술

Java, Kotlin, Spring Boot · Python, FastAPI, LangGraph, MCP · TypeScript, Next.js · PostgreSQL, PostGIS, Redis, Kafka · Docker, Kubernetes, Argo CD, Terraform, AWS · Prometheus, Grafana, Tempo, Loki, OpenTelemetry
