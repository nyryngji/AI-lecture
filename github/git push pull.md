## 📄 git push, pull

> **파일 생성** 

- code 파일.py : 파이썬 파일 생성 

  📌오류 발생 시 visual studio code의 bin 폴더를 환경변수에 추가
 
- python 파일.py : 파이썬 파일 실행 및 결과 출력
<br>

> **파일 수정 후** 
- staging area 상태 : 현재 basic 파일 존재(1줄)
>> 
- working directory 상태 : 파일 변화(modified) (2줄)

<br>

> **파일 삭제**
- unstage : staging area에서 파일 내리기 

- git rm --cached 파일.py : staging area에서 파일 삭제
 
- git rm --cached -f basic.py : 강제 삭제 (untracked 상태로 돌아감)

  📌 다시 git add 후 git rm --cached 파일.py 실행 시 잘 삭제됨 
  
  **-->** working과 staging에 있는 파일이 같기 때문 
  
  <br>
  
  > **파일 복구**
  - git restore --staged 파일.py : staging area를 이전으로 복구
  
  
