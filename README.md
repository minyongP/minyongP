<div align="center">

<img
  src="https://capsule-render.vercel.app/api?type=waving&color=0:0ea5e9,100:22c55e&height=130&section=header&text=%EC%95%88%EB%85%95%ED%95%98%EC%84%B8%EC%9A%94.%20%EB%B0%95%EB%AF%BC%EC%9A%A9%EC%9E%85%EB%8B%88%EB%8B%A4.&fontSize=40&fontColor=ffffff&animation=fadeIn"
  alt="안녕하세요. 박민용입니다."
/>

### Java · Spring Boot Backend Developer

</div>

- **성능 개선** — 쿼리 튜닝으로 조회 시간을 약 **99%**, API 응답 시간을 약 **46% 단축**했습니다. *(합성 벤치마크 기준)*
- **전체 구현** — 데이터 모델·API 설계부터 지도·필터·차트 화면 연동까지 구현해, 데이터 조회부터 사용자 화면까지 이어지는 기능을 완성했습니다.
- **아키텍처 설계** — 메일 전송을 비즈니스 트랜잭션에서 분리하고 DB Outbox·재시도를 적용해, 메일 서버 장애 시에도 요청을 보존하고 전송을 재개하도록 설계했습니다.

<div align="center">

<p>
  <img src="https://img.shields.io/badge/Java-000000?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
</p>

<p>JPA / Hibernate · MySQL · PostGIS · Redis · Amazon S3 · React<br>Docker · GitHub Actions · Flyway · JUnit 5 · Testcontainers · k6</p>

</div>

---

## 프로젝트

### [PinLog](https://github.com/Team-PinLog/PinLog) · 경험과 맥락을 기록하고 AI 검색으로 다시 찾는 장소 아카이빙 서비스

핵심 도메인·API 설계, 데이터 무결성 관리, 지도·피드 조회 성능 개선을 담당했습니다.

- **조회 성능 개선** — 실행 계획에 맞춰 정렬식과 인덱스를 정비해 피드 후보 쿼리를 **236.65 → 2.30ms**, 피드 API 중앙값을 **368 → 197ms**로 단축했습니다.
- **핵심 도메인 설계** — Record·Context·Collection·Follow의 데이터 모델과 API를 설계하고 DB 제약 조건으로 도메인 규칙을 반영했습니다.
- **데이터 정합성 관리** — 연관 데이터의 연쇄 삭제와 동시성 제어를 구현했습니다.
- **성능 회귀 검증** — Record 천만 건 규모의 합성 벤치마크 환경을 구성하고, 실행 계획 기반 회귀 테스트를 추가했습니다.

<sub>성능 수치는 합성 벤치마크 결과입니다. API는 워밍 3회 후 10회 측정한 중앙값이며, 쿼리 실행 시간과 별도로 측정했습니다.</sub>

### [UJAX](https://github.com/ujax-v2/UJAX) · 문제 관리·코드 실행·백준 제출·풀이 공유를 지원하는 알고리즘 스터디 서비스

워크스페이스 권한·가입 흐름, 커뮤니티, 이메일 인증·재시도, 외부 알림을 개발했습니다.

- **메일 장애 대응** — DB Outbox와 스케줄러로 메일 전송을 비즈니스 트랜잭션에서 분리하고 실패 요청의 재시도를 구현했습니다.
- **가입 상태 분리** — 가입 대기 정보와 실제 계정을 분리해 이메일 인증 완료 후 계정을 생성하고, 재요청·만료 정보 정리 흐름을 구현했습니다.
- **워크스페이스 접근 제어** — 역할별 권한과 가입 신청·승인·취소 API를 구현했습니다.
- **외부 알림 구조 개선** — 알림 예약·수정·취소와 실제 전송 책임을 분리하고, Mattermost 실전송과 구조화 로그로 처리 흐름을 검증했습니다.
- **실패 처리 테스트** — Outbox 처리·SMTP 전송·스케줄러·가입 대기 정리 배치의 테스트를 작성했습니다.

### [Home Search](https://github.com/kosta-team2/Home-Search) · 공공데이터 기반 아파트 정보·실거래가 지도 탐색 서비스

지역·단지·실거래 조회 API와 지도 탐색, 기간·면적 필터, 가격 차트 연동을 담당했습니다.

- **부동산 조회 API** — 단지 상세 정보와 실거래 목록을 제공하는 API를 구현했습니다.
- **조건별 거래 탐색** — 기간·면적 필터를 화면에 연결해 조건에 맞는 실거래 내역을 탐색하도록 구현했습니다.
- **지도·차트 연동** — 지도 탐색과 가격 차트를 연결해 위치와 거래 가격을 함께 확인할 수 있도록 구현했습니다.
- **지역 조회 검증** — 상위·하위 지역 조회와 존재하지 않는 지역의 예외 처리 테스트를 작성했습니다.

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:22c55e,100:0ea5e9&height=100&section=footer" alt="파랑·초록 웨이브 푸터" />

</div>
