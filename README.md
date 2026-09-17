안드로이드 개발자입니다.

기업용 메신저를 만듭니다. 금융과 공공 고객사에 온프레미스로 납품하는 제품이라
보안 인증과 고객사별 빌드 분기를 함께 다룹니다.
지금은 레거시 Java + XML 앱을 Kotlin + Compose 로 옮기고 있습니다.

만드는 것에 공통점이 있다면, **왜 그렇게 만들었는지를 코드 옆에 적어 두는 것**입니다.
아래 저장소들은 대부분 README 와 설계 문서가 코드만큼 있습니다.

---

## 만든 것

### [LogLens](https://github.com/choieuihyun/LogLens) — 안드로이드 로그 표준화

로그를 정해진 형식으로 찍게 만드는 라이브러리와, 그 형식을 읽어 필터링하고 집계하는 뷰어.
두 컴포넌트는 서로의 코드를 참조하지 않고 **로그 한 줄 형식만 공유**합니다.
뷰어를 좋게 만드는 것보다 로그가 일정한 모양으로 찍히게 만드는 쪽에 무게를 뒀습니다.

`Python` · `Kotlin` · `.aar 배포` — 현재 업무 제품에 적용 중

### [RoomEscapeServer](https://github.com/choieuihyun/RoomEscapeServer) — 취소표 감지 서버

예약 사이트를 주기적으로 훑다가 `예약 불가 → 가능` 으로 바뀌는 순간을 잡아냅니다.
변화를 감지하려면 과거를 기억해야 해서 서버가 필요했습니다.
매장 10곳의 응답 형식이 HTML, JSON, POST, 조각으로 제각각이라 어댑터로 흡수했고,
**어댑터를 쓰기 전에 매장별 요청과 판정 근거를 먼저 문서로 적었습니다.**

`Kotlin` · `Spring Boot` · `PostgreSQL` · `Docker` · `Caddy` — 오라클 클라우드에서 운영 중

### [Floduler](https://github.com/choieuihyun/RoomEscapeScheduler) — 일정 조합 계산기

겹치지 않는 모든 조합을 계산해 대기 시간이 어디에 얼마나 생기는지 보여줍니다.
예약 화면 캡처에서 회차 시간을 읽어오는데, **인식이 브라우저 안에서 돌아
이미지가 서버로 나가지 않습니다.** 의존성 0개, 정적 호스팅 하나로 배포됩니다.

`TypeScript` · `PaddleOCR(브라우저)` · `GitHub Pages` · 인수 테스트 44개

### [QuantTrading](https://github.com/choieuihyun/QuantTrading) — 종목 발굴 파이프라인

시세와 공시 재무를 모아 패턴별 후보를 추리고, 과거 시점 매수를 가정한 백테스트로 검증합니다.
스케줄 시각을 시장 구조에서 역산했습니다 — 장중에는 일봉이 미완성이라
거래량 비율이 왜곡되고, 그 값을 쓰는 패턴이 전부 탈락하기 때문입니다.

`Python` · `Next.js` · `GitHub Actions` · `Firestore` · `DART 공시 연동`

### [Personal Agent Harness](https://github.com/choieuihyun/Personal_Agent) — AI 오케스트레이션 골격

커맨드 하나가 서브에이전트를 순서대로 몰아 탐색 → 수정 → 빌드 → 런타임 검증까지 돌리고,
실패하면 분류해 재시도하거나 사람에게 넘깁니다.
**도구 권한은 프롬프트로 부탁하지 않고 설정으로 제한합니다.**
무한 루프는 시도 횟수와 반복 에러 상한으로 끊습니다.

`Python` · `Shell` — 업무에서 쓰던 파이프라인을 프로젝트 비의존 골격으로 추출

### [Algorithm](https://github.com/choieuihyun/Algorithm) — 알고리즘 연습

AI 가 코드를 대신 써 주는 환경일수록 직접 푸는 감각이 무뎌진다고 생각해 이어오고 있습니다.
2022년 12월 시작.

`Java`

---

## 쓰는 것

**주로** Kotlin · Java · Jetpack Compose · Android
**곁들여** Python · TypeScript · Spring Boot · PostgreSQL

**관심** 실시간 통신과 동기화, 모바일 보안 인증, 테스트 자동화
