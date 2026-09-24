# 홍성주

숭실대학교 컴퓨터학부에서 공부하는 백엔드·AI 시스템 엔지니어입니다.
모델의 출력이 실제 데이터, 사용자의 명시적 결정, 데모 뒤에도 계속 돌아가야 하는 시스템과 만나는 제품을 만듭니다.

[웹사이트](https://seongju.vercel.app) · [이메일](mailto:seongjuice999@gmail.com) · [English](./README.md)

## 현재

- **[TrabyOS](https://github.com/TrabyOS) Founding Engineer** · Mac에서 실시간 시장 정보를 묻고, 완성된 주문 카드를 확인한 뒤 음성으로 모의 주문을 승인·수정·취소하는 트레이딩 워크스페이스를 만들고 있습니다. [웹사이트](https://trabyos-website.vercel.app/) · [무료 테스트 빌드](https://github.com/TrabyOS/trabyos-test/releases/latest)
- **[비자르큐브 AI](https://www.bzrr.ai/) ([MXN Commerce Group](https://www.mxncommerce.com/en)) Software Engineer Intern** · 패션 이커머스 운영을 위한 실서비스 AI 에이전트를 만들고 있습니다. [GitHub](https://github.com/bizarrecube)
- **숭실대학교 컴퓨터학부** · 2022–현재. [전공 과제](https://github.com/ghdtjdwn/cs-coursework)

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

## 오픈소스

업스트림에 반영된 기여입니다. [전체 Pull Request 보기](https://github.com/search?q=is%3Apr+author%3Aghdtjdwn+-org%3Aghdtjdwn&type=pullrequests)

- [Ouroboros #2365](https://github.com/Q00/ouroboros/pull/2365) · 진행 중인 MCP 클라이언트 연결이 취소될 때 상태와 HTTP 자원이 남는 문제를 수정하고 회귀 테스트 6건을 추가했습니다.
- [Caveman #1013](https://github.com/JuliusBrussee/caveman/pull/1013) · 초기화 뒤 `--force`가 에디터 규칙 파일을 갱신하지 못하던 문제를 수정했으며, 작성자 이력을 보존한 후속 PR로 병합됐습니다.
- [psycopg #1345](https://github.com/psycopg/psycopg/issues/1345) · `AsyncConnectionPool.getconn()`이 취소를 삼키는 문제를 재현하고, 릴리스 전에 유지보수자의 수정 [#1407](https://github.com/psycopg/psycopg/pull/1407)을 검증했습니다.

## 수상

- 🏆 매니패스트 특별상 · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 은상 · 숭실대학교 컴퓨터학부 소프트웨어공모전 2026 · [참도미](https://github.com/chamdormie)
- 🏅 우수상 · 숭실대학교 솔브드 코드 알고리즘 대회 2025
