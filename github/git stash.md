## 📄 git stash

> **git stash**
 
- 커밋할 필요 없이 파일의 변경 사항을 stash 스택에 저장

- 저장 내용 : working directory와 staging area의 수정 내용

- 브랜치 이동 시 working directory가 깨끗한 상태가 되도록 설정 가능 

- 깨끗한 상태: 마지막 상태의 내용이 WD,SA에 똑같이 저장되어 있는 상태 

- stash 이후에는 WD, SA 가 동일
<br>

> **git stash 관련 명령어**

- **git stash (-m '메시지')** : 임시 저장

- **git stash branch [브랜치명]** : 새로운 브랜치를 만들고 임시저장 후 적용된 임시저장 삭제

- **git stash list** : git stash에 몇 개의 stash가 존재하는지 출력

  <img width="488" alt="캡처" src="https://user-images.githubusercontent.com/105197496/200762017-2f6b3cde-225e-4b9b-a6e5-888d8e842f3b.PNG">

- **git stash show** : 현재 working directory와 stash의 비교

  <img width="429" alt="캡처" src="https://user-images.githubusercontent.com/105197496/204323239-e9b21fd2-fea2-4a14-8c39-d612f28337cf.PNG">


- **git stash show -p** : git stash show를 더 자세히 보여줌

  <img width="488" alt="캡처" src="https://user-images.githubusercontent.com/105197496/200761889-15e91dd9-0e51-48c9-8a17-e5b0eb1c8d10.PNG">

- **git stash show stash@{i}** : WD와 지정된 stash를 비교
 
  - stash@{0}이 가장 최근 임시저장 

  - -p를 붙이면 좀 더 상세한 정보 확인 가능

  <img width="486" alt="33333" src="https://user-images.githubusercontent.com/105197496/200763903-a19910cf-2448-4096-8153-dde8bf80c852.PNG">

<br>

- **git stash pop** : 최근 또는 지정된 임시저장소 내용을 가져와 반영하고 삭제 

- **git stash apply** : **WD에만** 최근 또는 임시 저장소 내용을 가져와 반영

- **git stash apply --index** : WD, SA 두 곳에 동시 임시 저장

- **git stash apply --keep-index** : 현재 상태에서 staging area는 남기고 WD만 임시저장

- **git stash --include-untracked** : untracked 파일 임시 저장
<br>

- **git stash drop** : stash@{0} 삭제

  - **git stash drop stash@{숫자}** : 해당 번호 stash 목록 삭제 (목록이 0부터 시작함)

- **git stash clear** : stash 목록 전부 날리기

  <img width="458" alt="캡처" src="https://user-images.githubusercontent.com/105197496/204952299-75f3eb23-c75f-47e8-a6b2-05a832e4caa1.PNG">


- **git clean(-f)** : untracked 파일 삭제(강제 삭제)

- **git clean -n** : 만약에 지우면 무슨 파일이 지워지는지 확인 

  <img width="459" alt="캡처" src="https://user-images.githubusercontent.com/105197496/204952477-a6d245be-7522-4a51-9fe8-6a55851b1e3e.PNG">

- **git clean -i** : git clean에 대한 옵션 6가지를 제시 후 선택 가능하게 함 

  <img width="457" alt="캡처" src="https://user-images.githubusercontent.com/105197496/204952819-aab1da61-64e6-4ec2-9854-720cf4554eb8.PNG">

