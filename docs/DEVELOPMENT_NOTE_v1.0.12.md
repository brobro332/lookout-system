
### 5a7066a Prometheus 컨테이너 강제 재시작 (설정 갱신)
- **작업 파일**: docker-compose.yml
- **작업 목적**: 수정된 prometheus.yml이 컨테이너에 즉시 반영되지 않고 과거 설정을 물고 있는 현상 해결
- **작업 내용**:
  - docker-compose.yml의 prometheus 서비스에 더미 환경변수(FORCE_RELOAD_CONFIG=1)를 주입하여, docker compose up -d 실행 시 컨테이너가 강제로 Recreate 되면서 새로운 설정 파일(/actuator/prometheus)을 정상적으로 로드하도록 강제 트리거 반영
