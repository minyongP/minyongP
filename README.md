# 박민용 | Backend Developer

데이터와 지표로 병목을 찾고, 테스트와 문서로 개선을 증명하는 Java/Spring 백엔드 개발자입니다.  
기능 구현에 그치지 않고 데이터 구조, 장애 복구, 운영 환경까지 함께 살핍니다.

## 제가 중요하게 생각하는 것

- `EXPLAIN ANALYZE`와 부하 테스트 결과를 근거로 성능 문제를 좁혀갑니다.
- API 계약과 데이터 무결성을 테스트로 고정해 변경에 강한 서비스를 만듭니다.
- 설계 결정과 실패한 시도도 문서로 남겨 동료가 같은 맥락에서 이어갈 수 있게 합니다.

## 주요 프로젝트

### [PinLog Backend](https://github.com/Team-PinLog/back)

장소 기록과 컬렉션, 자연어 검색을 제공하는 서비스의 Spring Boot 백엔드를 개발했습니다.

- PostgreSQL generic plan 때문에 지도 조회가 16~22배 느려지는 조건을 재현하고 실행 계획을 분석했습니다.
- custom plan 적용 전후를 실데이터로 비교해 지도 API 응답을 `67.5ms → 38.8ms`, 키워드 API를 `72.1ms → 25.6ms`로 개선했습니다.
- 인증, 피드, 컬렉션, 커서 페이지네이션과 AI 비동기 연동을 구현하고 통합 테스트와 API 문서를 함께 관리했습니다.

### [Home Search](https://github.com/minyongP/Home-Search)

아파트 실거래 데이터를 수집·정규화하고 지도에서 탐색하는 서비스입니다.

- PostGIS 공간 조회와 인덱스를 조정해 지도 마커 API를 `48ms → 11ms`로 개선했습니다.
- K6 부하 테스트에서 p95 응답 시간을 `2초 → 1초 미만`으로 줄이고 성공률 `99% 이상`을 확인했습니다.
- 원본 데이터 보존, 중복 수집 방지, 매칭 실패 근거 추적을 중심으로 데이터 파이프라인을 설계했습니다.

### [UJAX](https://github.com/ujax-v2/ujax-server)

알고리즘 스터디를 위한 워크스페이스형 협업 플랫폼입니다.

- 회원가입 이메일 인증과 메일 아웃박스 구조를 정리했습니다.
- 웹훅 전송 계층을 분리하고 timeout 정책과 구조화 로그를 도입했습니다.
- 제출 연동과 코드 실행 기능을 운영하기 위한 서버 구조를 개선했습니다.

### [ARENA](https://github.com/SSAFY1516Final/ARENA)

서로 다른 관점의 AI가 사용자의 고민을 토론하고, 결과를 커뮤니티에 공유하는 서비스입니다.

- Spring AI 기반 후보 생성·검증·토론 파이프라인을 설계했습니다.
- Kakao OAuth, JWT 인증과 게시글·투표·댓글 기능을 구현했습니다.

## 기술

`Java` · `Spring Boot` · `Spring Security` · `JPA` · `MyBatis`  
`PostgreSQL` · `PostGIS` · `MySQL` · `Redis`  
`Docker` · `Kubernetes` · `GitHub Actions` · `Prometheus` · `Grafana`

## Contact

[Email](mailto:dev.my.park@gmail.com) · [GitHub](https://github.com/minyongP) · [Solved.ac](https://solved.ac/minon98)
