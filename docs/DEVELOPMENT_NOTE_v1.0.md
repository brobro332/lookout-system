# DEVELOPMENT NOTE v1.0

### 257e504 프로젝트 초기 파일 추가
- **작업 파일**: 모든 프로젝트 초기 설정 파일들
- **작업 목적**: lookout-system 신규 레포지토리 초기화 및 Spring Boot 기반 파일 구성
- **작업 내용**: 기본 디렉토리 구조, 빌드 스크립트(build.gradle), gitignore 등 초기 세팅

### 5bf5c1e 모니터링 인프라 구축
- **작업 파일**: docker-compose.yml, prometheus/prometheus.yml, loki/loki-config.yml, promtail/promtail-config.yml, alertmanager/alertmanager.yml
- **작업 목적**: Prometheus + Loki 모니터링 스택 뼈대 구성
- **작업 내용**:
  - docker-compose.yml 작성 및 각 모니터링 툴(Prometheus, Loki, Promtail, Grafana, Alertmanager) 배치
  - Promtail을 이용해 호스트의 Docker 로그 폴더 마운트 (애플리케이션 로그 무설정 자동 수집)
  - Grafana 접속 비밀번호를 환경변수로 분리
