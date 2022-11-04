## 📄 git stash

> **git stash**
 
- 커밋할 필요 없이 파일의 변경 사항을 stash 스택에 저장

- 저장 내용 : working directory와 staging area의 수정 내용

- 브랜치 이동 시 working directory가 깨끗한 상태가 되도록 설정 가능 

- 깨끗한 상태: 마지막 상태의 내용이 WD,SA에 똑같이 저장되어 있는 상태 
<br>

> **git stash 관련 명령어**

- **git stash list** : git stash에 몇 개의 stash가 존재하는지 출력

- **git stash show** : git stash가 현재 어떤 상태인지 출력

- **git stash show -p** : git stash show를 더 자세히 보여줌
<br>

- **git stash pop** : 최근 또는 지정된 임시저장소 내용을 가져와 반영하고 삭제 

- **git stash apply** : **WD에만** 최근 또는 임시 저장소 내용을 가져와 반영

- **git stash apply --index** : WD, SA 두 곳에 동시 임시 저장
<br>

- **git stash drop** : 맨 마지막 stash목록 삭제

  - **git stash drop stash@{숫자}** : 해당 번호 stash 목록 삭제 (목록이 0부터 시작함)

- **git stash clear** : stash 목록 전부 날리기

- **git clean(-f)** : untracked 파일 삭제(강제 삭제)

- **git clean -n** : 만약에 지우면 무슨 파일이 지워지는지 확인 

- **git clean -i** : git clean에 대한 옵션 6가지를 제시 후 선택 가능하게 함 
