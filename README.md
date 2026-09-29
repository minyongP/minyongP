<div align="center">

<img
  src="https://capsule-render.vercel.app/api?type=waving&color=0:0ea5e9,100:22c55e&height=130&section=header&text=%EC%95%88%EB%85%95%ED%95%98%EC%84%B8%EC%9A%94.%20%EB%B0%95%EB%AF%BC%EC%9A%A9%EC%9E%85%EB%8B%88%EB%8B%A4.&fontSize=40&fontColor=ffffff&animation=fadeIn"
  alt="안녕하세요. 박민용입니다."
/>

### Java · Spring Boot Backend Developer

</div>

Java·Spring Boot 기반의 백엔드 개발자입니다.

- **조회 성능** — 실행 계획을 분석해 쿼리와 인덱스를 개선합니다.
- **데이터 무결성** — 도메인 규칙을 데이터 모델과 DB 제약 조건에 반영합니다.
- **외부 연동 안정성** — 실패가 핵심 비즈니스 로직에 전파되지 않도록 분리하고 재시도 구조를 설계합니다.

변경 전후를 테스트와 측정으로 검증하고, 선택한 이유와 한계를 기록합니다.

<div align="center">

<p>
  <img src="https://img.shields.io/badge/Java-000000?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
</p>

<p>JPA / Hibernate · MySQL · Redis · Docker · GitHub Actions · k6</p>

</div>

---

## 프로젝트

### [PinLog](https://github.com/Team-PinLog/PinLog) · 데이터 모델과 조회 성능

경험과 맥락을 기록하고 AI 자연어 검색으로 다시 찾는 장소 아카이빙 서비스입니다.
**핵심 데이터 모델 및 API 설계와 데이터 무결성·조회 성능 개선을 담당했습니다.**

- **문제:** 피드 후보 조회가 상위 100건을 반환하기 위해 약 66만 건을 정렬했습니다.
- **판단과 변경:** 실행 계획에서 정렬식과 인덱스의 불일치를 찾아 수정했습니다. DB 제약 조건을 확인해 변경 전후 결과가 같음을 검증했습니다.
- **결과:** 합성 벤치마크 환경에서 해당 쿼리는 **236.65 → 2.30ms**, 피드 API는 **중앙값 368 → 197ms**로 개선했습니다. 실행 계획을 확인하는 회귀 테스트도 추가했습니다.

<sub>Record 천만 건 규모의 벤치마크 결과입니다. API 수치는 워밍 3회 후 10회 측정한 중앙값이며, 쿼리 측정과 구분합니다.</sub>

[내 기여와 측정 조건](docs/pinlog.md) · [피드 조회 병목 분석 및 개선 PR](https://github.com/Team-PinLog/back/pull/183) · [핵심 도메인 설계 PR](https://github.com/Team-PinLog/back/pull/51)

`Java` · `Spring Boot` · `PostgreSQL` · `Redis` · `Kafka`

### [UJAX](https://github.com/ujax-v2/UJAX) · 권한과 외부 연동 안정성

문제 관리부터 코드 실행, 백준 제출과 풀이 공유까지 이어지는 알고리즘 스터디 워크스페이스입니다.
워크스페이스 권한·가입 흐름과 커뮤니티, 이메일 인증·재시도 및 외부 알림을 개발했습니다.

- **문제:** 회원가입·초대 메일의 전송 실패가 비즈니스 처리에 영향을 주고, 실패한 요청을 다시 처리할 구조가 필요했습니다.
- **판단과 변경:** 메일 요청을 DB Outbox에 저장하고 스케줄러가 전송·재시도하도록 분리했습니다. 가입 대기 정보와 실제 계정을 분리해, 이메일 인증을 완료한 경우에만 계정을 생성하도록 바꿨습니다.
- **결과:** 메일 서버 장애가 가입·초대 요청의 DB 트랜잭션에 직접 영향을 주지 않도록 전송 책임을 분리했고, 실패 요청을 재시도할 수 있는 구조를 만들었습니다.
- **검증:** Outbox 처리·메일 전송·스케줄러 테스트를 작성했습니다. 외부 알림은 실제 Mattermost 전송과 구조화 로그로 처리 흐름을 확인했습니다.

[내 기여와 설계 범위](docs/ujax.md) · [메일 Outbox와 이메일 인증 PR](https://github.com/ujax-v2/ujax-server/pull/85) · [외부 알림 책임 분리 및 검증 PR](https://github.com/ujax-v2/ujax-server/pull/97)

`Java` · `Spring Boot` · `MySQL` · `Redis`

### [Home Search](https://github.com/kosta-team2/Home-Search)

공공데이터로 아파트 정보와 실거래가를 지도·차트에서 탐색하는 서비스입니다.
단지 상세·실거래 목록 API를 구현하고, 지도 탐색과 기간·면적 필터, 가격 차트를 화면에 연결했습니다.

[지역 조회 API와 테스트](https://github.com/kosta-team2/home-server/pull/8) · [단지 상세 조회 API](https://github.com/kosta-team2/home-server/pull/13) · [실거래 목록 API](https://github.com/kosta-team2/home-server/pull/23)

`Java` · `Spring Boot` · `PostgreSQL / PostGIS` · `React`


<img src="https://capsule-render.vercel.app/api?type=waving&color=0:22c55e,100:0ea5e9&height=100&section=footer" alt="파랑·초록 웨이브 푸터" />

</div>
