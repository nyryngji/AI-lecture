## 📄 git reset, revert 

> **git reset**

- **git reset** : 커밋 이력 재설정 수행  

  - 되돌린 이후 커밋 이력 제거 (= 특정 커밋으로 되돌아가기 )
  
  - ex) 커밋이 1 2 3 4 5 6이 있는데 2로 이동시 3 4 5 6 이력 삭제됨

  - **BEFORE**
  <img width="430" alt="reset before" src="https://user-images.githubusercontent.com/105197496/203697837-07dca9ec-84a1-40c5-b38d-a1a1ef48086f.PNG">

  - **AFTER**
  <img width="430" alt="reset after" src="https://user-images.githubusercontent.com/105197496/203697861-02bf23c2-ef10-4f6c-b552-f07da6b73751.PNG">

  - reset 후 WD는 그대로, Staging area는 한 줄이 줄어든 것을 확인 가능
  <img width="429" alt="리셋 후 wd는 그대로 staging은 한줄 없어짐" src="https://user-images.githubusercontent.com/105197496/203697936-ec11712c-7176-4f87-93de-8c1e58c5087d.PNG">

<br>

- **git reset --soft** : reset 이후 커밋 내용만 수정

  - 바로 다시 커밋 가능한 상태로 남아있음 
  
  - 다시 마지막 이전 head로 돌아가려면 commit만 하면 됨
<br>

- **git reset --mixed** : reset 이후 커밋 내용과 staging 가 같음, working 수정 안함

  - head 내용을 stage에 복사 
  
  - 다시 이전으로 돌아가려면 add, commit 필요 
<br>

- **git reset --hard** : reset 이후 커밋 내용=wd=staging 모두 동일

  - head 내용을 wd에 복사, stage에 복사 
  
  - 다시 이전으로 돌아가려면 수정, add, commit 필요 

  - **BEFORE**
  <img width="430" alt="git reset --hard" src="https://user-images.githubusercontent.com/105197496/203700509-a5c61e37-c875-4583-b0b1-8ab362f929b1.PNG">
  
  - **AFTER**
  <img width="429" alt="git reset --hard after" src="https://user-images.githubusercontent.com/105197496/203700561-47a9cb85-3994-4d36-8f2b-5f57aaec1fbb.PNG">

<br>

- 세가지 모두 head가 이동하려는 커밋아이디로 이동

- **git reset --hard orig_head** : reset 이후 다시 원상태로 되돌리기

- **git reflog** : 모든 커밋 이력을 보여줌 
  
  <img width="431" alt="git reflog" src="https://user-images.githubusercontent.com/105197496/203700855-e3ea520f-c229-42bf-9445-6079e1fc3919.PNG">

<br>

> **git revert**

- **git revert** : 특정 커밋 이력을 **취소**하고 바로 이전 상태로 돌아가는 방법 수행

  - 현재까지의 커밋이력에 되돌아간 커밋 이력이 추가됨
  
  - a b c d가 있을 때 git revert b 하면 a로 이동

  - **BEFORE**
  <img width="429" alt="revert 전" src="https://user-images.githubusercontent.com/105197496/203701125-90ddec38-75e4-4ac2-9d1c-9803ac13ce7e.PNG">

  - **AFTER**
  <img width="429" alt="revert 후" src="https://user-images.githubusercontent.com/105197496/203701220-46f15d4d-49ac-4cff-9299-6a5e9c2af684.PNG">

- **git revert [커밋아이디]** : 커밋을 추가로 수행

  - 기본 편집기에서 커밋 메시지 편집 화면 실행 

- **git revert head --no-edit** : 편집 화면 없이 이전 커밋 메시지가 커밋메시지로 사용됨
<br>

> **깃허브**

- **WD** : 개발자가 직접 코드를 수정하는 공간 의미 (.git을 제외한 모든 영역에 해당)

- **Index** : WD에서 저장소로 정보가 저장되기 전 준비 영역 (.git/index 파일로 관리)
 
- **저장소** : 파일이나 폴더를 변경 이력 별로 저장해두는 영역 (이력이 남는 유일한 곳)
 
- **Stash** : 임시적으로 작업 사항 저장 후 나중에 꺼내올 수 있는 영역 

