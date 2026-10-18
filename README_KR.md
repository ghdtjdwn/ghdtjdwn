# 홍성주

숭실대학교 컴퓨터학부에서 공부하는 백엔드·AI 시스템 엔지니어입니다.
모델의 출력이 실제 데이터, 사용자의 명시적 결정, 데모 뒤에도 계속 돌아가야 하는 시스템과 만나는 제품을 만듭니다.

[웹사이트](https://seongju.vercel.app) · [이메일](mailto:seongjuice999@gmail.com) · [English](./README.md)

## 현재

- **[TrabyOS](https://github.com/TrabyOS) Founding Engineer** · 말로 실제 암호화폐 거래를 해주는 음성 트레이딩 비서입니다. 현물·무기한 선물 주문을 말하면 주문 카드로 보여주고, 승인하면 거래소에서 주문을 실행합니다. 시세·잔고·뉴스도 물어볼 수 있습니다. [웹사이트](https://trabyos-website.vercel.app/)
- **[비자르큐브 AI](https://www.bzrr.ai/) ([MXN Commerce Group](https://www.mxncommerce.com/en)) Software Engineer Intern** · 패션 이커머스 운영을 위한 실서비스 AI 에이전트를 만들고 있습니다. [GitHub](https://github.com/bizarrecube)
- **숭실대학교 컴퓨터학부** · 2022–현재. [전공 과제](https://github.com/ghdtjdwn/cs-coursework)

## 수상

- 🏆 매니패스트 특별상 · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 은상 · 숭실대학교 컴퓨터학부 소프트웨어공모전 2026 · [참도미](https://github.com/chamdormie)
- 🏅 우수상 · 숭실대학교 솔브드 코드 알고리즘 대회 2025

## 오픈소스

업스트림에 병합된 변경 7건과, 메인테이너 요청으로 재현·검증한 수정 1건입니다. 작업이 깊었던 순서로 적었습니다. [전체 Pull Request 보기](https://github.com/search?q=is%3Apr+author%3Aghdtjdwn+-org%3Aghdtjdwn&type=pullrequests)

- **[OpenTelemetry Python Contrib #5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032)** · WSGI에서 요청 헤더로 샘플링 판단하기

  WSGI 미들웨어가 요청 헤더를 서버 span이 만들어진 뒤에야 수집해서, 샘플러가 헤더를 보고 판단할 수 없었습니다. 설정으로 지정하고 민감 값을 가린 헤더를 span 생성 시점에 넘기도록 바꿨고, 내부 span과 메트릭에는 헤더가 들어가지 않는 기존 동작을 유지했습니다. 한 달간 리뷰를 거쳐 세 명의 승인으로 병합됐으며, 메인테이너가 올린 추적 이슈 [#4975](https://github.com/open-telemetry/opentelemetry-python-contrib/issues/4975)의 WSGI 항목에 해당합니다.

  이어서 [Falcon #5160](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5160), [Flask #5161](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5161), [Pyramid #5162](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5162)의 후속 변경을 리뷰하고 로컬에서 테스트해, 캡처한 헤더가 샘플러에 전달되면서 메트릭에는 들어가지 않는지 확인했습니다. 세 PR 모두 2026년 10월 16일 병합되면서 추적 이슈의 작업이 완료됐습니다.

- **[OpenTelemetry Python #5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681)** · 계측 테스트용 공용 `CapturingSampler`

  위 변경을 리뷰하던 메인테이너가 계측마다 테스트용 샘플러를 따로 만들지 말고 하나를 같이 쓰자고 요청해, 코어 저장소의 `opentelemetry-test-utils`에 추가했습니다. 테스트는 이 샘플러로 span 시작 시점에 샘플러가 받는 속성을 확인합니다. 1.45.0 릴리스에 포함됐고, 이후 Django와 aiohttp-server 계측 테스트에서도 쓰이고 있습니다.

- **[OpenTelemetry Python Contrib #5170](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5170)** · Tornado에서 캡처하는 헤더의 민감 값 가리기와 정규식 매칭

  Tornado는 HTTP 서버 계측 가운데 유일하게 캡처할 헤더 이름을 글자 그대로만 찾고 `OTEL_INSTRUMENTATION_HTTP_CAPTURE_HEADERS_SANITIZE_FIELDS`를 무시해서, 민감한 헤더 값이 span에 그대로 기록될 수 있었습니다. WSGI·aiohttp-server 계측과 같은 공용 헬퍼를 쓰도록 바꿔, 헤더 이름은 대소문자 구분 없이 정규식으로 매칭하고 민감한 헤더 값은 `[REDACTED]`로 기록합니다. 캡처한 헤더가 샘플러에도 전달되는 [#4975](https://github.com/open-telemetry/opentelemetry-python-contrib/issues/4975) 작업을 하다 발견했고, 메인테이너 두 명의 승인으로 병합됐습니다.

- **[Ouroboros #2365](https://github.com/Q00/ouroboros/pull/2365)** · MCP 클라이언트 연결이 취소될 때의 정리

  `MCPClientAdapter.connect()`를 도중에 취소하면 어댑터가 연결된 상태로 남고 HTTP 클라이언트도 닫히지 않는 문제를 발견해 [#2364](https://github.com/Q00/ouroboros/issues/2364)로 보고했습니다. 취소를 전파하기 전에 상태를 되돌리고 직접 만든 클라이언트를 닫도록 고쳤으며, 다른 정리 단계가 실패해도 닫습니다. 회귀 테스트 6건을 추가했고, 메인테이너 두 명의 승인을 받아 v0.54.5에 포함됐습니다.

- **[psycopg #1345](https://github.com/psycopg/psycopg/issues/1345)** · 비동기 풀에서 취소가 사라지는 문제의 재현과 수정 검증

  `AsyncConnectionPool.getconn()`이 연결 검사 중에 발생한 취소를 삼켜, 이미 취소된 호출자에게 연결을 돌려주는 경우가 있었습니다. 계측을 넣어 이 보고를 재현하고 결정적인 회귀 테스트를 공유했으며, 메인테이너 요청으로 [#1407](https://github.com/psycopg/psycopg/pull/1407)의 수정이 문제를 해결하는지 확인했습니다. 수정 코드는 메인테이너가 작성했고 psycopg_pool 3.3.2로 배포됐습니다.

- **[Micrometer #7925](https://github.com/micrometer-metrics/micrometer/pull/7925)** · Java `HttpClient` 관측의 사용자 정의 태그 문서

  2024년부터 열려 있던 문서 요청 [#4962](https://github.com/micrometer-metrics/micrometer/issues/4962)를 해결했습니다. `HttpClientObservationConvention`으로 기본 태그를 유지하면서 태그를 추가하는 방법을 레퍼런스 문서에 넣었습니다. 예제는 실제로 요청을 보내고 기록된 타이머를 검증하는 테스트에서 가져오므로, 프로젝트와 함께 컴파일되고 테스트됩니다.

- **[Ponytail #828](https://github.com/DietrichGebert/ponytail/pull/828)** · Pi 확장에서 `/tree` 이동 후 모드 복원

  `/ponytail off` 뒤에 `/tree`로 이전 브랜치에 돌아가도 Ponytail이 꺼진 채로 남았습니다. 확장이 저장된 모드를 세션 시작 때만 복원했기 때문입니다. 트리 이동 때도 복원하도록 고쳐, 주입되는 지침과 상태 표시줄이 선택한 브랜치의 모드를 따릅니다. v4.13.0에 포함됐습니다.

- **[Caveman #1013](https://github.com/JuliusBrussee/caveman/pull/1013)** · `--force`로 기존 에디터 규칙 파일 갱신

  이미 초기화한 저장소에서 `caveman-init --force`를 실행해도 Cursor·Windsurf·Cline 규칙 파일을 설치된 것으로 보고 건너뛰어, 오래된 규칙이 그대로 남았습니다. 한 글자를 고치고 회귀 테스트 3건을 추가했습니다. 메인테이너가 제 커밋을 [#1015](https://github.com/JuliusBrussee/caveman/pull/1015)에 체리픽해 병합했고 v2.7.0에 포함됐습니다.

## 제품

### [ssu 캠퍼스 AI](https://github.com/ghdtjdwn/ssuAI)

학생이 학교 공개 정보와 자신의 학사·LMS·도서관 데이터를 하나의 웹 앱이나 자연어 에이전트에서 찾고 활용합니다. 명시적인 승인 경계를 둔 MCP 도구 52개를 [ssuAI](https://github.com/ghdtjdwn/ssuAI), [ssuMCP](https://github.com/ghdtjdwn/ssuMCP), [ssuAgent](https://github.com/ghdtjdwn/ssuAgent), [ssu-ai-service](https://github.com/ghdtjdwn/ssu-ai-service)가 나누어 제공합니다. [서비스 열기](https://ssuai.vercel.app)

`Spring Boot` `LangGraph` `Next.js` `Kubernetes`

### [그늘](https://github.com/ghdtjdwn/geuneul)

15만 건이 넘는 공공 장소에서 가까운 그늘과 폭염 대피시설을 찾는 여름 생존 지도입니다. PostGIS로 반경·최근접 검색을 처리하고, 이용자의 현장 제보는 지도를 새로고침하지 않아도 실시간으로 도착합니다. [지도 열기](https://geuneul.vercel.app)

`Spring Boot` `PostGIS` `SSE` `Terraform`

### [참도미](https://github.com/chamdormie)

학생의 조건을 기숙사 모집요강과 비교해 어떤 자격을 충족하거나 놓쳤는지 보여 주고, 그 결과를 룸메이트 탐색으로 이어 줍니다. 여덟 가지 생활 성향의 추천 근거, 모집글, 참여 신청과 승인, 1:1·단체 채팅으로 추천에서 실제 방 구성까지 연결합니다. [참도미 열기](https://chamdomi.vercel.app)

`Spring Boot` `Next.js` `MySQL` `WebSocket`

### [marketvalley](https://github.com/unithon26)

초기 창업자가 문제와 솔루션을 한 번 입력하면 하나의 검증 가설에서 공개 랜딩, 소셜 카드 5장, 문구와 Meta 광고를 만듭니다. 이후 실제 Insights, 방문, 동의 기반 예약을 모아 다음 검증 여부를 사람이 판단할 수 있게 돌려줍니다. [서비스 열기](https://marketvaley.vercel.app) · [소스 코드](https://github.com/unithon26/marketvalley)

`Next.js` `Supabase` `Anthropic` `Meta Marketing API`

### [Folding](https://github.com/dotenv-uploaded)

HWP·Office·PDF를 위한 로컬 우선 데스크톱 워크스페이스입니다. 선택한 폴더 전체에 질문하고 원문 근거와 문서 관계를 확인한 뒤, 원본을 조용히 덮어쓰지 않고 새 파일을 만들어 다시 검증하는 형식별 편집을 승인할 수 있습니다. [소스 코드](https://github.com/dotenv-uploaded/_FOLDING_)

`Electron` `FastAPI` `Gemma 4` `SQLite`

### [흥할지도](https://github.com/ghdtjdwn/heungmap)

한국관광공사 데이터로 기획자와 방문객을 연결하는 축제 기획·탐색 서비스입니다. 축제 관람객 수가 아니라 행사 30일 전에 알 수 있는 시군구 전체 방문자-일의 범위와 요인, What-if 비교를 제공합니다. 채택한 계절 기준선과 LightGBM 잔차 모델은 시간 홀드아웃에서 WAPE 3.939%를 기록했고, 기획 보고서가 모델 입력에 없는 숫자를 만들면 서버에서 거부됩니다.

`FastAPI` `LightGBM` `Next.js` `Claude`
