# Docker
1. 도커
- 2013년 공개된 컨테이너 기반의 오픈소스 가상화 프랫폼
- 소프트웨어를 "컨테이너"라는 표준화된 유닛으로 패키징하여 사용하는 방식
- 컨테이너에는 라이브러리, 시스템 도구, 코드, 런타임 등 소프트웨어 실행에 필요한 모든 것이 포함됨

2. 방식 비교
기존방식  vs 도커 컨테이너 방식
MySQL 설치  MySQL 이미지
MySQL 실행  MySQL 컨테이너 실행

3. 도커 컴포넌트
1) Docker Engine
  (1) Docker Image 생성
  (2) Docker Container 생성 및 실행
  (3) Docker 명령어 실행
2) Docker Registry
  (1) Docker Hub
3) Docker Compose
  (1) 여러 개의 Docker Container를 관리하기 위한 툴
  (2) 여러 Docker Container의 구성 정보를 yml 형식으로 정의
4) Docker Swarm
  (1) Docker Host들을 클러스터로 구성해서 관리하는 오케스트레이션 툴
  (2) Kubernates가 사실상 Docker Swarm을 대체하였음

4. Docker Image
1) 컨테이너를 만들기 위한 읽기 전용 플랫폼
2) 애플리케이션 실행에 필요한 모든 파일, 설정, 라이브러리 등이 포함됨
3) 한 번 생성된 이미지는 불변성의 특징을 가짐
4) 레이어 구조를 가지고 있어서 효율적인 저장이 가능합

5. Docker Container
1) 이미지를 실행한 실제 프로세스 (동작하는 애플리케이션)
2) 격리된 환경에서 이미지가 제공한 것을 이용해 애플리케이션이 실행되는 구조
3) 호스트 OS와 분리되어 독립적으로 작동
4) 한 번 실행된 컨테이너는 수정하지 않고 폐기함

| 구분   | 프로그램           | 프로세스                        |
|--------|--------------------|---------------------------------|
| 저장 위치 | 디스크(SSD/HDD)   | 메모리(RAM)                     |
| 상태   | 정적(실행 전)      | 동적(실행 중)                   |
| 개수   | 파일은 1개         | 동시에 여러 개 실행 가능         |
| 예시   | `chrome.exe`       | `chrome.exe` (탭 5개 열렸을 때) |


도커 이미지   받기   : docker image pull 이미지명
도커 컨테이너 만들기 : docker container create --name 컨테이너명 이미지명
              시작   : docker container start 컨테이너명
              종료   : docker container stop 컨테이너명
              삭제   : docker container rm 컨테이너명
* docker container run
