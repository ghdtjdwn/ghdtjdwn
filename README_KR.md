**백엔드·인프라·AI 제품을 만듭니다. 동시성·데이터 정합성부터 배포·관측·복구까지 설계합니다.**

[LinkedIn](https://www.linkedin.com/in/ghdtjdwn/) · [이메일](mailto:seongjuice999@gmail.com) · [English](./README.md)

## 경력

- [비자르큐브 AI](https://www.bzrr.ai/) Software Engineer Intern (2026.09 ~ ) · [조직](https://github.com/bizarrecube)
- [젝트(JECT)](https://ject.kr/) Backend & Infrastructure Engineer (2026.10 ~ ) · [내 PR](https://github.com/JECT-Study/Billit-5th-Server/pulls?q=is%3Apr+author%3Aghdtjdwn+is%3Amerged) · [인프라 저장소](https://github.com/JECT-Study/Billit-5th-Infra)
- [TrabyOS](https://github.com/TrabyOS) 공동창업 팀 기술 총괄 (2026.09 ~ 2026.10)
- 숭실대학교 컴퓨터학부 (2022.03 ~ 2027.02 졸업 예정) · [12개 과목의 전공 학습 기록](https://github.com/ghdtjdwn/cs-coursework)
- 대한민국 육군 군 복무 (2023.05 ~ 2024.11)

## 오픈소스

외부 저장소 6곳에 PR 10건이 병합되거나 반영됐습니다. 관측성, 취소 처리, 회귀 테스트가 중심입니다.

| 프로젝트 | 바꾼 것 | 상태 |
|---|---|---|
| [OpenTelemetry Python](https://github.com/open-telemetry/opentelemetry-python/pulls?q=is%3Apr+author%3Aghdtjdwn) | 메인테이너가 [요청한](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5073#discussion_r4061037725) 공용 테스트 샘플러 `CapturingSampler`. contrib 패키지 18개의 테스트가 사용합니다 | 1.45.0 배포 · [#5681](https://github.com/open-telemetry/opentelemetry-python/pull/5681) |
| [OpenTelemetry Python Contrib](https://github.com/open-telemetry/opentelemetry-python-contrib/pulls?q=is%3Apr+author%3Aghdtjdwn) | 샘플링 시점의 요청 헤더 전달(WSGI), 리뷰에서 찾은 헤더 마스킹 누락(Tornado), 기본 타임아웃 유지(urllib), span 생성 시 클라이언트 속성 전달(Tornado), 헤더 수집 문서(Starlette) | 병합 · [#5032](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5032) · [#5170](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5170) · [#5347](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5347) · [#5348](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5348) · [#5356](https://github.com/open-telemetry/opentelemetry-python-contrib/pull/5356) |
| [Micrometer](https://github.com/micrometer-metrics/micrometer) | Java HttpClient 관측의 사용자 정의 태그 문서와, 테스트가 컴파일·실행하는 예제 | 1.16.8 · 1.17.2 배포 · [#7925](https://github.com/micrometer-metrics/micrometer/pull/7925) |
| [Ouroboros](https://github.com/Q00/ouroboros) | MCP 초기화가 취소되면 HTTP 자원과 연결 상태를 정리하고 회귀 케이스 6건 추가 | v0.54.5 · [#2365](https://github.com/Q00/ouroboros/pull/2365) |
| [Ponytail](https://github.com/DietrichGebert/ponytail) | 대화 트리를 이동하면 선택한 분기의 저장된 모드 복원 | v4.13.0 · [#828](https://github.com/DietrichGebert/ponytail/pull/828) |
| [Caveman](https://github.com/JuliusBrussee/caveman) | 규칙 강제 갱신 복구 | v2.7.0에 체리픽 · [#1013](https://github.com/JuliusBrussee/caveman/pull/1013) |

[psycopg #1345](https://github.com/psycopg/psycopg/issues/1345)에서는 비동기 풀의 취소 유실을 재현하고 메인테이너의 수정을 검증했습니다(psycopg_pool 3.3.2).

**리뷰 중** · [OpenTelemetry](https://github.com/open-telemetry/opentelemetry-python-contrib/pulls?q=is%3Apr+is%3Aopen+author%3Aghdtjdwn) · [Lettuce #3909](https://github.com/redis/lettuce/pull/3909) · [Spring AI #6929](https://github.com/spring-projects/spring-ai/pull/6929) · [slowapi #305](https://github.com/laurentS/slowapi/pull/305)

## 수상

- 🏅 **우수상** · 2026 관광데이터 활용 공모전 웹·앱 구현 부문 · 한국관광공사 · [흥할지도](https://github.com/ghdtjdwn/heungmap)
- 🏆 **매니패스트 특별상** · UNITHON 2026 · [marketvalley](https://github.com/unithon26/marketvalley)
- 🥈 **은상** · 숭실대학교 컴퓨터학부 소프트웨어공모전 2026 · [참도미](https://github.com/chamdormie)
- 🏅 **우수상** · 숭실대학교 솔브드 코드 알고리즘 대회 2025

## 프로젝트

- **[ssu 캠퍼스 AI](https://github.com/ghdtjdwn/ssuMCP)** · 숭실대 학사·도서관·강의 기능을 웹과 MCP 도구 52개로 제공. 서비스 4개를 혼자 개발·운영. **같은 좌석 동시 예약 100건 → 학교 시스템 쓰기 1회.** [부하 시험](https://github.com/ghdtjdwn/ssuMCP/blob/main/docs/performance/library-agent-load-test.md) · [웹 앱](https://ssuai.vercel.app)
- **[흥할지도](https://github.com/ghdtjdwn/heungmap)** · 축제 기획자를 위한 지역 방문 수요 예측. **WAPE 4.256% → 3.939%**, 4,959 지역·일 시간 홀드아웃. [모델 카드](https://github.com/ghdtjdwn/heungmap/blob/main/docs/MODEL_CARD.md) · [서비스](https://heungmap.vercel.app)
- **[그늘](https://github.com/ghdtjdwn/geuneul)** · 공공 장소 15만여 곳과 실시간 제보를 보여 주는 여름 쉼터 지도. **점수 검색 SQL 361ms → 172ms**, 합성 장소 30만 건 로컬 측정. [EXPLAIN 비교](https://github.com/ghdtjdwn/geuneul/blob/main/perf/explain/RESULTS.md) · [지도 열기](https://geuneul.vercel.app)
- **[marketvalley](https://github.com/unithon26/marketvalley)** · 창업 아이디어 하나로 소개 페이지·카드뉴스·Meta 광고를 만들고 실제 반응을 수집. `SKIP LOCKED`·lease·체크포인트 기반 PostgreSQL 작업 큐. [아키텍처](https://github.com/unithon26/marketvalley/blob/main/docs/architecture.md)
- **[참도미](https://github.com/chamdormie)** · 생활 습관 8가지로 기숙사 룸메이트를 추천하고 모집·채팅까지 연결. 화면, 룸메이트 도메인, 애플리케이션 배포 담당. [서비스 열기](https://chamdomi.vercel.app)

<sub>성능 수치는 측정 조건을 담은 자료로 연결했습니다. 팀 프로젝트는 제 담당 범위를 적었습니다.</sub>
