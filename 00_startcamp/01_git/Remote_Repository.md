# git을 외부로 공유하려면?
## Remote Repository - GitLab, GitHub
- GitLab은 Private, GitHub는 Public 느낌
- SSAFY에서는 교육생 대상 발급된 GitLab을 활용하고, 개인 능력을 보여줄 수 있는 포폴은 GitHub로 관리해야함
- GitHub에서 Create Repository할 때, Add a README 체크 여부?
  - 원격 저장소에서 처음 Commit할거면 체크
  - 로컬에서 먼저 작업하고 업로드할거면 체크 안함
- git remote add origin https://github.com/ygujg/01_git_Review.git
  - 로컬 저장소에 원격 저장소를 추가할건데, origin이라는 이름이고 주소는 다음과 같다는 뜻
- git remote -v: 등록된 원격 저장소 목록 확인
- git remote rm origin: origin 원격 저장소 삭제
- git push origin master: 원격 저장소에 `Commit 목록`을 업로드
  - origin 원격 저장소에 master라는 이름의 branch를 push
  - 최초 push할 때에는 GitHub로부터 인증서(git credential) 발급 필요 - 해당 원격 저장소에 push할 권한이 있는 확인