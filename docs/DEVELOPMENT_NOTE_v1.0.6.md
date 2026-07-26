
### a3b848b Alertmanager 포트 충돌 해결
- **작업 파일**: docker-compose.yml
- **작업 목적**: Kafka와의 호스트 포트 충돌(9093) 방지
- **작업 내용**:
  - lertmanager가 호스트로 노출하는 포트를 9093에서 9095로 변경 (9095:9093)
