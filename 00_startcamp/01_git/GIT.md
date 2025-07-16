# GIT
- 분산 버전 관리 시스템
- 코드의 변경 이력을 기록하고 협업을 원활하게 하는 도구
- 각 버전은 이전 버전으로부터의 변경사항을 기록
- 원본을 두 사람이 복제해가서 서로 다른 작업을 한 후 합치면 충돌 발생
  - GIT을 활용하면, 버전이 기록돼있어 원본 손실없이 버전 충돌이 일어난 부분만 수정하면 해결

# GIT의 3가지 영역
- Working Directory(WD)
  - 실제 작업 중인 파일들이 위치하는 영역
- Staging Area(SA)
  - WD에서 변경된 파일 중 다음 버전에 포함시킬 파일들을 선택적으로 추가하거나 제외할 수 있는 중간 준비 영역
  - 기능 하나 추가할 때마다 버전 나누면 좋음

- Repository: 버전 이력과 파일들이 영구적으로 저장되는 영역
  - 모든 버전과 변경 이력 기록
  - 버전을 Commit(저장, snapshot)하면 SA있는 내용은 삭제
---
- git init: 로컬 저장소 설정(초기화)
  - 현재 WD를 git으로 버전 관리하겠다는걸 선언
  - GUI 상 폴더 내용 변화가 없으면, 폴더에서 보기 > 숨긴 항목 누르면 보임
  - 숨겨진 항목은 안건드리는 것이 좋음
  - git의 관리를 받기 시작한 WD는 (master) 가 뒤에 붙음
  - rm -rf ~/Desktop/study/00_startcamp/01_git/.git: git 버전 관리 해제
    - `맨 뒤에 .git 안붙이면 디렉토리 통째로 날아감 ㅠㅠ`

- git add: 변경사항이 있는 파일을 SA에 추가
- git commit -m '버전 이름': SA에 있는 파일들을 저장소에 기록
  - 해당 시점 버전을 생성하고 변경 이력 남김
  - 최초 commit하기 위해선 이메일과 이름 등록해야하는데, global로 전역 등록하면 다음부턴 등록 안해도 됨
  - git config --global user.email '메일 주소'
  - git config --global user.name '이름'
  - 등록된 정보 확인하려면 list
    - git config --global --list
  - 수정하고 싶으면
    - code ~/.gitconfig
  - 만약 여러 계정으로 관리하려면 global 말고 local 써야하는데 필요하면 따로 찾아보자

- git status: commit 현황, SA에 등록/등록되지 않은 파일 표시
  - SA 등록 후 commit 하기 전에 파일을 수정 후 저장해보자. status 보면 변경 사항 있다고 알려줌

- git log: 누가 언제 수정했는지 표시
  - Open repository 메뉴 눌러도 확인 가능
