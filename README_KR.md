**백엔드·인프라·AI 제품을 만듭니다. 동시성·데이터 정합성부터 배포·관측·복구까지 설계합니다.**

사용자에게 필요한 제품, 명확한 시스템 보장, 구현을 입증하는 근거를 연결합니다. 음성 트레이딩 제품의 창업 개발과 실서비스 AI 에이전트 개발을 하며, 시스템의 기반이 되는 오픈소스에도 기여하고 있습니다.

[LinkedIn](https://www.linkedin.com/in/ghdtjdwn/) · [이메일](mailto:seongjuice999@gmail.com) · [English](./README.md)

## 경력

- **Co-founder & CTO · [TrabyOS](https://trabyos.com)** - 음성 트레이딩 제품의 백엔드와 네이티브·웹 통합을 포함한 개발 전반을 이끌고 있습니다.
- **Software Engineer Intern · [비자르큐브 AI](https://www.bzrr.ai/) / [MXN Commerce Group](https://www.mxncommerce.com/en)** - 패션 이커머스 운영을 위한 실서비스 AI 에이전트를 개발하고 있습니다. [조직](https://github.com/bizarrecube)
- **숭실대학교 컴퓨터학부 · 2022–현재** - [12개 과목의 전공 학습 기록](https://github.com/ghdtjdwn/cs-coursework).
- **군 복무 · 대한민국 육군** - 2023.05–2025.11.

## 오픈소스

**6개 업스트림 저장소에 변경 7건 반영.** 직접 병합된 PR 6건과 메인테이너가 체리픽한 변경 1건입니다. 관측성, 취소 처리, 상태 정합성, 회귀 검증에 집중합니다. **2026-10-19 상태 확인.**

### [OpenTelemetry](https://github.com/open-telemetry) · 하나의 계측 결함에서 공통 테스트 기반으로

- **메인테이너의 요청으로 개별 테스트를 코어 공용 유틸로 확장.** WSGI 수정 PR을 리뷰하던 OpenTelemetry 메인테이너가 [샘플러를 코어 테스트 유틸에서 공용으로 사용할 수 있게 해 달라고 요청](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032#discussion_r4061074604)했습니다. 이를 `CapturingSampler`로 구현해 **1.45.0 릴리스에 반영**했으며, 현재 WSGI·Django·ASGI·aiohttp-server·Falcon·Flask·Pyramid·Tornado의 **HTTP 계측 8종의 테스트**에서 재사용됩니다. [Core #5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681) · [사용 사례](https://github.com/open-telemetry/opentelemetry-python-contrib/blob/de43f819a4a919213d246a23e62a1b256aeca7b9/instrumentation/opentelemetry-instrumentation-asgi/tests/test_asgi_custom_headers.py)
- **샘플링 시점에 헤더를 전달하도록 수정.** WSGI에서 span 생성 시 마스킹한 요청 헤더를 넘기고, 내부 span과 메트릭에는 포함하지 않도록 했습니다. 메인테이너 3명의 승인을 받아 병합됐습니다. [Contrib #5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032)
- **후속 적용과 추가 결함까지 추적.** 다른 계측의 **후속 PR 6건**을 검증·리뷰했습니다. 이 과정에서 Tornado가 민감 헤더 마스킹 설정을 무시하는 문제를 발견하고 공용 캡처 헬퍼로 수정했습니다. [Contrib #5170](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5170) · [추적 이슈 #4975](https://github.com/open-telemetry/opentelemetry-python-contrib/issues/4975)

### 다른 개발자의 시스템에서도 동작하는 신뢰성 개선

- **[Ouroboros #2365](https://github.com/Q00/ouroboros/pull/2365) · 취소 시 자원 정리 - 병합, v0.54.5.** MCP 초기화 취소 시 HTTP 자원 누수와 연결 상태 잔류를 수정하고 **회귀 테스트 6건**을 추가했습니다.
- **[psycopg #1345](https://github.com/psycopg/psycopg/issues/1345) · 비동기 풀 취소 처리 - 재현·검증 기여.** 취소 유실을 재현하고 결정적 회귀 테스트를 제공한 뒤 메인테이너의 수정을 검증했습니다. 수정은 psycopg_pool 3.3.2로 배포됐으며, 이 기여는 위 변경 7건과 별도입니다.
- **[Micrometer #7925](https://github.com/micrometer-metrics/micrometer/pull/7925) · 검증되는 관측성 문서 - 병합.** Java HttpClient 관측의 사용자 정의 태그 문서와 실제 컴파일·실행되는 검증 예제를 추가했습니다.
- **[Ponytail #828](https://github.com/DietrichGebert/ponytail/pull/828) · 분기별 상태 복원 - 병합, v4.13.0.** 대화 트리 이동 시 선택한 분기의 저장된 모드가 복원되도록 수정했습니다.
- **[Caveman #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · 강제 갱신 복구 - v2.7.0 반영.** **에디터 3종**의 규칙 파일 갱신을 복구하고 회귀 테스트를 추가했습니다. 메인테이너가 [#1015](https://github.com/JuliusBrussee/caveman/pull/1015)에 체리픽해 병합했습니다.

## 수상

- 🏆 **매니패스트 특별상** · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 **은상** · 숭실대학교 컴퓨터학부 소프트웨어공모전 2026 · [참도미](https://github.com/chamdormie)
- 🏅 **우수상** · 숭실대학교 솔브드 코드 알고리즘 대회 2025

<details>
<summary><h2>프로젝트 8개 · 실험 · 사용 기술 펼쳐보기</h2></summary>

## 프로젝트

### [TrabyOS](https://trabyos.com) · 말로 요청하고, 확인한 주문을 실행하는 거래 워크스페이스

**Co-founder & CTO.** 웹과 macOS에서 시세를 묻고, 주문을 검토·수정한 뒤 승인하여 본인의 거래소 계좌에서 실행하는 제품입니다. 파트너 플랫폼을 위한 음성 기술도 제공합니다.

- **여러 언어와 화면을 하나의 실행 경로로 통합.** Python 오케스트레이션, Spring Boot 서비스, Swift 네이티브 UI와 웹을 연결해 시장 데이터·계좌 상태·주문 흐름을 다룹니다.
- **의도 해석과 실행 권한을 분리.** 자연어로 동작을 준비하고, 명시적인 사용자 승인과 결정론적 검사로 실행을 통제합니다. 종목·수량·계좌 상태를 거래 계약의 일부로 유지합니다.
- **대화 밖의 제품 경험까지 구현.** 거래소 연동, 실시간 갱신, 온보딩, 패키징과 배포를 함께 다룹니다.

`Python` · `Java / Spring Boot` · `Swift / SwiftUI` · `TypeScript` · `PostgreSQL / WebSocket`

[공식 웹사이트](https://trabyos.com) · [GitHub 조직](https://github.com/TrabyOS)

### ssu 캠퍼스 AI · 사용자의 의도를 실제 학사 작업까지 연결하는 플랫폼

[ssuAI](https://github.com/ghdtjdwn/ssuAI) · [ssuMCP](https://github.com/ghdtjdwn/ssuMCP) · [ssuAgent](https://github.com/ghdtjdwn/ssuAgent) · [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service)

학교 공개 정보와 개인 학사·LMS·도서관 데이터를 웹 앱과 에이전트에서 활용합니다. 커넥터와 에이전트부터 배포·관측까지 **4개 서비스로 구성된 플랫폼**을 만들었습니다.

- **웹 앱과 MCP 서버로 같은 캠퍼스 기능 제공.** 학교 정보 조회와 학사·LMS·도서관 작업을 **MCP 도구 52개**로 제공해 Claude Desktop·Cursor 같은 MCP 클라이언트에서도 사용할 수 있습니다. REST와 MCP는 같은 서비스 계층을 사용하고, LangGraph가 전문 에이전트 라우팅·대화 영속화·쓰기 전 승인을 관리합니다. [MCP 연결 안내](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/mcp-tools.md)
- **100명 예약 경합 → 외부 쓰기 1회.** Intent 큐와 동일 좌석 중복 억제로 학교 시스템을 보호했습니다. WireMock 대상 동시 요청 100건으로 검증했으며, 처리 지연을 감수하고 외부 쓰기를 줄인 설계입니다. [부하 시험 근거](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/performance/library-agent-load-test.md)
- **배포부터 장애 관측까지 운영.** ARM64 이미지를 GitHub Actions·GHCR·ArgoCD로 k3s에 배포하고, Prometheus/Grafana·Tempo·Loki로 메트릭·트레이스·로그를 연결했습니다. 장애 주입으로 서킷브레이커의 차단과 복구까지 확인했습니다. [관측성·장애 대응 기록](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/troubleshooting-highlights.md)

`Java / Spring Boot` · `Python / LangGraph` · `PostgreSQL / Redis` · `k3s / ArgoCD` · `OpenTelemetry`

[웹 앱](https://ssuai.vercel.app) · [챗봇](https://ssuai.vercel.app/chat)

### [marketvalley](https://github.com/unithon26/marketvalley) · 하나의 가설에서 시장 검증 전체 흐름으로

**백엔드·AI·플랫폼 담당.** 창업자가 문제와 해결책을 한 번 입력하면 랜딩, **소셜 카드 5장**, 문구와 Meta 광고를 만들고 실제 Insights·방문·동의 기반 사전예약을 모아주는 팀 제품입니다.

PostgreSQL 작업 큐, `SKIP LOCKED`, lease, operation key와 checkpoint로 생성·광고 생성·결과 수집을 브라우저 탭의 수명과 분리했습니다. 외부 작업의 중복 실행을 제어하면서 실패한 단계부터 재시도할 수 있게 했습니다. [아키텍처](https://github.com/unithon26/marketvalley/blob/main/docs/architecture.md)

🏆 **UNITHON 2026 매니패스트 특별상.**

`Next.js` · `Supabase / PostgreSQL` · `Anthropic` · `Meta Marketing API`

[조직](https://github.com/unithon26) · [소스·팀 역할](https://github.com/unithon26/marketvalley) · [라이브 서비스](https://marketvaley.vercel.app)

### [그늘](https://github.com/ghdtjdwn/geuneul) · 가까운 쉼터를 빠르게 찾는 여름 생존 지도

**15만 건 이상의 공공 장소**에서 그늘·쉼터를 찾고 현장 제보를 실시간으로 확인합니다. 데이터 수집, 공간 검색 백엔드, 애플리케이션과 인프라를 구현했습니다.

- **실행계획으로 실제 병목을 특정.** 공간 인덱스는 이미 동작하고 있었지만, 점수 검색마다 만료된 제보를 다시 훑고 있었습니다. 만료 필터에 인덱스를 추가해 SQL 실행 시간을 **361 → 172ms, 약 52% 단축**했습니다. 동일한 합성 장소 30만 건·제보 21만 건을 로컬 QEMU 환경에서 비교한 결과입니다. [EXPLAIN 비교](https://github.com/ghdtjdwn/geuneul/blob/main/perf/explain/RESULTS.md)
- **수집부터 화면 갱신까지 반복 가능하게.** 멱등 ETL, PostGIS 반경·최근접 검색, SSE 제보, 코드로 관리하는 인프라를 연결했습니다.

`Spring Boot` · `PostgreSQL / PostGIS` · `SSE` · `Terraform / AWS`

[소스·아키텍처](https://github.com/ghdtjdwn/geuneul) · [지도 열기](https://geuneul.vercel.app)

### [참도미](https://github.com/chamdormie) · 기숙사 자격 확인에서 실제 룸메이트 구성까지

**프런트엔드·룸메이트 도메인·통합·애플리케이션 인프라 담당.** **8가지 생활 성향**의 설명 가능한 추천, 모집·신청 흐름, 1:1·단체 채팅을 구현했습니다. 애플리케이션의 Spring Boot/MySQL 배포, Helm 구성, 네트워크 격리, 이미지 digest 검증과 백업·복구 검증 조건을 담당했습니다.

🥈 **숭실대학교 컴퓨터학부 소프트웨어공모전 2026 은상.** 팀과 함께 기숙사 입주 자격 확인부터 룸메이트 구성까지 연결했습니다.

`Spring Boot` · `Next.js` · `MySQL` · `WebSocket` · `Helm`

[조직](https://github.com/chamdormie) · [서비스 열기](https://chamdomi.vercel.app)

### [흥할지도](https://github.com/ghdtjdwn/heungmap) · 예측 결과를 기획자의 판단으로 연결

**백엔드·데이터·모델·통합 담당.** 관광 데이터를 바탕으로 축제 기획과 방문객 탐색을 연결합니다. 행사 30일 전의 정보 제약을 두고 **시군구 방문자-일**의 범위와 기여 요인을 예측합니다.

- **WAPE 4.256% → 3.939%.** 계절 기준선에 LightGBM 잔차 모델을 더해 **4,959 지역·일의 후향 시간 홀드아웃**에서 WAPE를 **상대 7.43% 개선**했습니다. [모델 카드](https://github.com/ghdtjdwn/heungmap/blob/main/docs/MODEL_CARD.md)
- **실제 행사 100건 중 예측 가능 30 → 98건.** 날짜 구간과 행정구역 이력 처리를 보정해 지원 범위를 넓혔습니다. 이 수치는 예측 정확도가 아니라 제공 범위이며, 예측 대상도 축제 관람객 수가 아닌 지역 방문자-일입니다. [의사결정 기록](https://github.com/ghdtjdwn/heungmap/blob/main/docs/DECISION_LOG.md)
- **생성 보고서의 수치까지 통제.** API에서 근거 없는 수치를 거부하고, 정기 재학습은 5개 채택 조건을 통과한 모델만 반영하도록 구성했습니다.

`FastAPI` · `LightGBM / pandas` · `Next.js` · `Claude` · `정기 데이터 파이프라인`

[소스](https://github.com/ghdtjdwn/heungmap) · [라이브 서비스](https://heungmap.vercel.app)

### [Folding](https://github.com/dotenv-uploaded/_FOLDING_) · 문서 전체에 질문하고, 변경을 승인하는 작업 공간

**에이전트 백엔드·파일 작업 경계 담당.** HWP·Office·PDF를 위한 로컬 우선 워크스페이스입니다. FastAPI sidecar, 에이전트 오케스트레이션, 승인, 파일 수정·Undo, 지식 동기화를 구현했습니다. 검색은 원문 근거를 제시하고, 승인된 편집은 원본을 보존하면서 새 파일을 생성·검증합니다.

`FastAPI` · `Electron` · `SQLite` · `로컬 LLM`

[조직](https://github.com/dotenv-uploaded) · [제품 저장소](https://github.com/dotenv-uploaded/_FOLDING_) · [에이전트 백엔드](https://github.com/dotenv-uploaded/_FOLDING_/tree/main/services/agent) · [로컬 실행](https://github.com/dotenv-uploaded/_FOLDING_#running-locally)

### [Billit · JECT](https://github.com/JECT-Study/Billit-5th-Infra) · 팀이 반복해서 사용할 수 있는 배포 기반

**팀 인프라 담당.** 운영 애플리케이션, 운영 데이터, 개발·모니터링을 분리한 **OCI ARM 서버 3대**의 인프라 기반을 구성했습니다.

- **한 번 빌드한 이미지를 환경 간 승격.** 공통 GitHub Actions 워크플로가 ARM64 이미지를 빌드하고 개발에 배포한 뒤 운영으로 수동 승격하도록 구성했습니다. 환경별 배포 조정과 상태 검사 실패 시 이전 이미지 복구로 배포 경로를 보호합니다.
- **배포 이후의 운영까지 포함.** OpenTofu·Docker Compose·Nginx·PostgreSQL/Redis·백업·Prometheus/Loki/Grafana를 연결했습니다. 격리 통합 환경에서 배포와 대기 시간 초과 동작을 확인했으며, 실제 애플리케이션 배포 연결을 진행 중입니다.

`OCI / OpenTofu` · `GitHub Actions / GHCR` · `Docker / Nginx` · `PostgreSQL / Redis` · `Prometheus / Grafana / Loki`

[JECT](https://github.com/JECT-Study) · [인프라](https://github.com/JECT-Study/Billit-5th-Infra) · [백엔드](https://github.com/JECT-Study/Billit-5th-Server) · [프런트엔드](https://github.com/JECT-Study/Billit-5th-Client)

## 이전 제작물·실험

| 작업 | 구현·검증한 내용 |
| :--- | :--- |
| [Macro](https://github.com/UNITHON24/Macro) · [UNITHON24](https://github.com/UNITHON24) | 기존 키오스크 소프트웨어의 음성 접근성 클라이언트. 좌표 기반 자동화를 UIA/OCR·실행 후 상태 확인·SQLite 멱등 큐로 재설계. 기록상 테스트 76건과 Linux/Windows CI. |
| AI말평 실험 | **인코더 backbone 19종·설정 24개**를 nested OOF로 비교하고, 최종 후보를 prompt-LOPO·데이터 누출 검사와 배포 제약으로 추가 검증. |
| AXWAR 제출물 | 근거 기반 FAQ·공시 요약·환불 계산의 3개 파이프라인에서 모델의 문장 생성과 결정론적 수치·근거 검증을 분리. |

## 사용하는 기술

| 영역 | 기술 |
| :--- | :--- |
| **백엔드·데이터** | Java · Spring Boot · Python · FastAPI · PostgreSQL/PostGIS · MySQL · Redis |
| **인프라·관측성** | Docker · Kubernetes/k3s · ArgoCD · GitHub Actions · Terraform/OpenTofu · AWS/OCI · OpenTelemetry · Prometheus/Grafana · Tempo/Loki |
| **AI·제품 통합** | LangGraph · MCP · RAG · LightGBM · TypeScript/Next.js · Swift/SwiftUI |

<sub>성능 수치는 측정 조건을 담은 자료로 연결했습니다. 개인 담당 범위와 팀 전체의 제품 성과를 구분해 적었습니다.</sub>

</details>
