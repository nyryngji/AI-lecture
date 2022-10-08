## 📄 git branch 

> **브랜치 개요**

- 여러 개발자들이 동시에 다양한 작업을 수행할 수 있게 만들어주는 기능

- 각각의 브랜치는 다른 브랜치의 영향을 받지 않음 

- 저장소를 처음 만들면 git은 바로 main(master) 브랜치를 생성 
<br>

> **브랜치 장점**

- 작업의 기록을 그때그때 남기게 되므로 문제 발생시 원인을 찾거나 대책을 세우는 데 용이 

> **브랜치 종류**
<br>

> **브랜치 명령어** 

- **git branch** : 저장소 목록 보기
<img width="528" alt="git branch" src="https://user-images.githubusercontent.com/105197496/194698307-1839fc00-2a85-4f32-9923-c1723940697c.PNG">

- **git branch -a** : 원격 서버와 접속되어있는 저장소 포함 모든 저장소 목록을 보여줌 (없으면 지역 저장소 보여줌)

- **git branch new_name** : 저장소 생성

- **git checkout -b(=git switch -c)** : 저장소를 생성하고 바로 이동
<img width="537" alt="git checkout-b" src="https://user-images.githubusercontent.com/105197496/194698396-1c198275-45a1-4830-a724-9f09128585a9.PNG">

- **git branch -d 브랜치 이름** : 저장소 삭제 

  - 현재 자기 자신이 위치한 곳에서는 삭제 불가 

- **git branch -D 브랜치 이름** : 저장소 강제 삭제

- **git checkout -** : 이전 브랜치로 이동

- **git branch -v** : 브랜치 이름, 커밋 ID, 커밋 메시지까지 출력 (git branch에 비해 더 자세한 정보)
<img width="548" alt="git branch -v" src="https://user-images.githubusercontent.com/105197496/194698495-30e87c56-08f7-4d9c-8968-42f3360f7bff.PNG">

- **git switch(=checkout) 브랜치 이름** : 해당 브랜치로 이동

- **git log --graph -all** : 모든 브랜치의 커밋 내역 및 브랜치의 흐름을 보여줌  

- **git log --oneline --graph --all** : 모든 브랜치의 커밋 내역 및 브랜치의 흐름을 간단하게 보여줌  
<img width="726" alt="git log --graph --oneline" src="https://user-images.githubusercontent.com/105197496/194698754-791a61ee-14c9-48e2-b9cf-99e791d9abfe.PNG">
