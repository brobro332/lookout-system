
### 27935bb 도커 포트 충돌 수정 및 프로메테우스 타겟 변경
- **작업 파일**: docker-compose.yml, prometheus/prometheus.yml
- **작업 목적**: 배포 시 발생하는 포트 충돌(8080) 해결
- **작업 내용**:
  - datt-platform이 이미 8080 포트를 점유 중이므로, lookout-api의 외부 노출 포트를 8082로 변경 (8082:8080)
  - prometheus.yml에서 lookout-api를 긁어갈 때 같은 도커 네트워크 내부 통신을 하도록 lookout-api:8080으로 타겟 변경
