# 생각을 멈추면 안된다!

## 개인 프로젝트

### [Personal Agent Harness](https://github.com/choieuihyun/Personal_Agent) — AI 오케스트레이션 골격

- 어느 프로젝트를 하던 간에 직접 커스텀한 AI 오케스트레이션을 해당 도메인에 적용 가능하도록 모듈화.
- 파이썬 패키지로 설치 가능

커맨드 하나가 서브에이전트를 순서대로 몰아 탐색 → 수정 → 빌드 → 런타임 검증까지 돌리고,
실패하면 분류해 재시도하거나 사람에게 넘깁니다.
**도구 권한은 프롬프트로 부탁하지 않고 설정으로 제한합니다.**
무한 루프는 시도 횟수와 반복 에러 상한으로 끊습니다.

`Python` · `Shell` — 업무에서 쓰던 파이프라인을 프로젝트 비의존 골격으로 추출

### [LogLens](https://github.com/choieuihyun/LogLens) — 안드로이드 로그 표준화

로그를 정해진 형식으로 찍게 만드는 라이브러리와, 그 형식을 읽어 필터링하고 집계하는 뷰어.
두 컴포넌트는 서로의 코드를 참조하지 않고 **로그 한 줄 형식만 공유**합니다.
뷰어를 좋게 만드는 것보다 로그가 일정한 모양으로 찍히게 만드는 쪽에 무게를 뒀습니다.

`Python` · `Kotlin` · `.aar 배포` — 현재 업무 제품에 적용 중

### [RoomEscapeServer](https://github.com/choieuihyun/RoomEscapeServer) — 취소표 감지 서버

- 아래의 RoomEscapeScheduler와 연계된 서버입니다.
- 방탈출 동호회 인원들이 좀 더 원활한 방탈출 예약이 가능하도록 하는 방탈출 일정 크롤링, 취소표 알림 기능을 제공합니다.

매장 10곳의 응답 형식이 HTML, JSON, POST, 조각으로 제각각이라 어댑터로 흡수했고,
**어댑터를 쓰기 전에 매장별 요청과 판정 근거를 먼저 문서로 적었습니다.**

`Kotlin` · `Spring Boot` · `PostgreSQL` · `Docker` · `Caddy` — 오라클 클라우드에서 운영 중

### [Floduler](https://github.com/choieuihyun/RoomEscapeScheduler) — 일정 조합 계산기

- RoomEscapeServer와 연계된 프론트
- 겹치지 않는 모든 조합을 계산해 대기 시간이 어디에 얼마나 생기는지 보여줍니다.
- Server를 통해 실제 방탈출 회차 불러오기가 가능하고, 이미지 혹은 시간 직접 입력으로도 시간대 입력이 가능합니다.
- 이미지 인식의 경우 예약 화면 캡처에서 회차 시간을 읽어오는데, **인식이 브라우저 안에서 돌아 이미지가 서버로 나가지 않습니다.** 정적 호스팅 하나로 배포됩니다.

`TypeScript` · `PaddleOCR(브라우저)` · `GitHub Pages` · 인수 테스트 44개

### [QuantTrading](https://github.com/choieuihyun/QuantTrading) — 종목 발굴 파이프라인

시세와 공시 재무를 모아 패턴별 후보를 추리고, 과거 시점 매수를 가정한 백테스트로 검증합니다.
스케줄 시각을 시장 구조에서 역산했습니다 — 장중에는 일봉이 미완성이라
거래량 비율이 왜곡되고, 그 값을 쓰는 패턴이 전부 탈락하기 때문입니다.

`Python` · `Next.js` · `GitHub Actions` · `Firestore` · `DART 공시 연동`

### [Algorithm](https://github.com/choieuihyun/Algorithm) — 알고리즘 연습

- AI를 사용하는 요즘 시대에, 생각하는 힘이 약해지는 것 같아 약간 꾸준히 하는 알고리즘 풀이.

---

## 쓰는 것

**주로** Kotlin · Java · Jetpack Compose · Android
**곁들여** Python · TypeScript · Spring Boot · PostgreSQL

**관심** 실시간 통신과 동기화, 모바일 보안 인증, 테스트 자동화
