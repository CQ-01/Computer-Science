### 다른 변경사항과의 충돌 오류
- bash창에서 linux 커맨드를 이용하여 적용할 branch 선택하여 해결
- 먼저 git pull로 원격 저장소 파일을 내려받아 해결

### push, commit등 동작이 없는 오류
```bash
Another git process seems to be running in this repository
```
- git process가 다른 곳에서 동작하고 있어서 안됨
- process를 강제종료 시키면 해결
  - cmd : `rm -f ./.git/index.lock` 
  - powershell : `Remove-Item -Path "./.git/index.lock" -Force`

### 용량 제한 오류
- 100mb 이상의 파일 push 할때 깃허브 에러 발생
- Git LFS 기능 활용 시도 결과 실패
  - .gitignore 파일 확장자 문제?

### 로컬에 없는 데이터를 push 하려는 오류
- 로컬 파일 및 커밋 내의 파일 삭제 커맨드 입력결과 실패
- git 파일을 삭제했다가 새로 remote연결하여 해결