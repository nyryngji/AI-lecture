## 📄 git merge

> **merge**

- 여러 개의 브랜치를 하나로 모음
<br>

> **Fast-Forward merge**
 
- merge할 대상이 현재 커밋의 직접적인 뿌리가 되는 경우 
- 병합할 브랜치의 조상이 기준 브랜치인 경우
- 단순히 main 브랜치가 이동 
- main 브랜치에서 병합 필요
<br>

> **3-way merge**

- 두 브랜치의 조상이 같은 경우  
- 충돌 우려 있음 
-> 충돌 발생 시 add, commit 진행 후 병합된 이전 브랜치 삭제
<br>

> **merge 명령어**

- **git merge [브랜치명]** : 보통의 병합

  - 현 브랜치가 병합할 브랜치와 Fast Forward 관계 시 병합할 브랜치로 이동

  - 현 브랜치가 병합할 브랜치와 Fast Forward 관계 없을 시 병합할 브랜치와 병합

- **git merge [브랜치명] --no-ff** : 브랜치 관계에 상관없이 필요한 commit만 가져오기 가능 

  - 어떤 브랜치에서 merge를 했는지 기록 가능

  - 무조건 3- way merge에서만 

- **git merge --squash** : 

- **git branch --merged** : 병합된 브랜치 목록 보기 
 
  <img width="410" alt="캡처" src="https://user-images.githubusercontent.com/105197496/201929098-535d27e0-f4ff-43a3-a7c1-2d706980fc7c.PNG">

- **git branch --no-merged** : 병합되지 않은 브랜치 목록 보기

- **git reset --hard head^** : 바로 전 병합 취소

  <img width="410" alt="캡처2" src="https://user-images.githubusercontent.com/105197496/201929993-0b2a1128-eade-4c46-b92a-39be50d4148e.PNG">

