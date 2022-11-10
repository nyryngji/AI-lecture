## 📄 branch rebase

> **rebase** 

- **git rebase [브랜치명]** : [브랜치명]에 해당하는 커밋 이력을 모아놓은 이후에 현재 위치해있는 브랜치의 커밋이력을 정렬

  - **BEFORE**
  
  <img width="391" alt="캡처" src="https://user-images.githubusercontent.com/105197496/200976074-f644cd73-23f1-4904-b40f-4a5073258a80.PNG">

  
  - **AFTER**
  
  <img width="392" alt="캡처2" src="https://user-images.githubusercontent.com/105197496/200976092-c38c07eb-678a-43d7-87fd-c4897e82d898.PNG">

  - rebase 이후 반드시 main에서 rebase를 사용한 브랜치를 fast-forward 병합해야 함
  
  <img width="391" alt="캡처3" src="https://user-images.githubusercontent.com/105197496/200976978-06525b29-1de3-406e-b056-e719d1e9dac9.PNG">

- **git rebase --abort** : rebase 취소 

  - **BEFORE**
  
  <img width="390" alt="abort 전" src="https://user-images.githubusercontent.com/105197496/200978198-913a311f-5c6b-4ec6-89c0-34479c66139f.PNG">
  
  - **AFTER**

  <img width="390" alt="abort 후" src="https://user-images.githubusercontent.com/105197496/200978233-d40c3771-fd47-4ceb-a68b-3c18f03c590c.PNG">

- **git rebase --continue** : 

- **git rebase -i head~4** : head~3부터 수정 가능 
<br>

> **rebase 충돌 시 해결방법**

- 1) 파일 수정 

- 2) git add 

- 3) rebase --continue
