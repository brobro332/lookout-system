
### 4550dfe Prometheus 메트릭 수집 경로 버그 수정
- **작업 파일**: prometheus/prometheus.yml
- **작업 목적**: datt-platform 컨테이너(spring-boot-app)의 메트릭이 그라파나에서 조회되지 않는 현상 해결
- **작업 내용**:
  - spring-boot-app의 Actuator 엔드포인트 수집 경로가 /api/actuator/prometheus로 잘못 설정되어 있어 404 에러가 발생하던 것을 기본 경로인 /actuator/prometheus로 수정
