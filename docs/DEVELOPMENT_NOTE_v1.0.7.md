
### 5212b52 Loki 설정 파일 문법(스키마) 에러 수정
- **작업 파일**: loki/loki-config.yml
- **작업 목적**: Loki 컨테이너 기동 실패 에러(ield shared_store not found in type compactor.Config) 해결
- **작업 내용**:
  - 최신 버전의 Loki(3.x)에서 더 이상 지원하지 않는(Deprecated) shared_store 옵션을 설정 파일에서 제거
