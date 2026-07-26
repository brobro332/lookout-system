
### 821f909 Alertmanager 클러스터 모드 비활성화
- **작업 파일**: docker-compose.yml
- **작업 목적**: Alertmanager 기동 시 발생하는 gossip mesh 에러(unable to initialize gossip mesh) 해결
- **작업 내용**:
  - lertmanager 컨테이너 명령어에 --cluster.listen-address= 옵션을 추가하여 단일 노드 모드로 기동하도록 수정
