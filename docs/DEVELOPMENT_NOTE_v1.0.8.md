
### 4b71df8 Loki 보관주기 설정 오류 및 API 앱 종료 문제 해결
- **작업 파일**: loki/loki-config.yml, build.gradle
- **작업 목적**: 배포 후 Loki와 lookout-api 컨테이너가 무한 재시작(Restarting)되는 현상 수정
- **작업 내용**:
  - loki-config.yml: retention_enabled 사용 시 필수로 요구되는 delete_request_store: filesystem 속성 추가
  - uild.gradle: spring-boot-starter-web 의존성을 추가하여 앱이 바로 종료(exit 0)되지 않고 내장 톰캣으로 계속 구동되도록 수정
