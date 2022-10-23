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
<br>

> **다양한 commit 정보 확인**
- git log head^ : 이전 커밋부터 모든 커밋 내역 출력

- git log --pretty=short : git log에서 날짜만 없어짐

- git log --patch : git log + git show (모든 로그에서 수정한 줄을 비교)

- git log --stat : 통계정보를 보여줌  

- git show : 하나의 파일에 대한 수정 이력까지 보여줌

- git show head^ : 제일 최근 커밋 바로 이전 커밋의 수정 이력 출력 
<br>

> **원격 저장소 복제와 수정내용 가져오기**

- **git clone** 저장소 주소 (이름): 원격 저장소를 지역 저장소에 복제

  📌 이름을 붙이면 새 폴더를 만들고 거기에 저장소 복제

- git remote : 원격 저장소 별칭 이름 조회

- git remote -v : 원격 저장소 별칭 이름 세부 조회

- git clone 깃허브 주소 -o 원격저장소 별칭 : clone과 동시에 원격 저장소 별칭 지정 

  - git remote add 원격저장소 별칭 깃허브 주소 : 원격 저장소 별칭 지정

- **git pull** : 원격 저장소의 수정 내용을 다시 지역 저장소로 내려받기

  - clone 이후 수정사항이 발생했을 때 수정 사항 가져오기

- **git push** : 지역 저장소의 수정 내용을 다시 원격 저장소로 올리기

  📌 깃허브 저장소를 수정할 수 있는 권한이 있어야 함

- **fork** : 타인의 원격 저장소를 자신의 깃허브 원격 저장소에 복사

- **pull request** : 타인의 깃허브의 내용 수정(pull)을 요청하는 끌기 요청
