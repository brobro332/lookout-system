
### 2021cd5 Promtail 로그 수집 권한 문제 해결
- **작업 파일**: docker-compose.yml
- **작업 목적**: Promtail이 호스트의 Docker 로그 디렉토리(/var/lib/docker/containers)를 읽지 못해 메타데이터(라벨) 수집이 누락되는 현상 수정
- **작업 내용**:
  - promtail 컨테이너 옵션에 user: root 속성을 추가하여 최고 관리자 권한으로 호스트의 로그 파일들에 접근할 수 있도록 권한 부여
