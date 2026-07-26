
### fd02678 도커 외부 네트워크 이름 정확도 수정
- **작업 파일**: docker-compose.yml, .github/workflows/deploy.yml
- **작업 목적**: 외부 네트워크(datt-network) 연결 오류 수정
- **작업 내용**:
  - 사용자 의견을 반영하여 deploy.yml에 임시 추가했던 네트워크 자동 생성 로직 롤백
  - lookout-system의 docker-compose.yml에서 외부 네트워크를 datt-platform이 생성한 실제 이름(datt-platform_datt-network)으로 정확히 매핑
