## 깃 명령어

> **기본**
- **pwd** : 현재 자기가 위치하고 있는 폴더 확인 
- git --help : 도움말 보기 
- git --version : 버전 보기 
- git config --list : 전체 설정 확인 (로컬, 전역 저장소 이름, 이메일 확인 가능)
<br>

> **사용자 설정**
- git config --global user.name(email) 사용할 이름/이메일 : 모든 git 작업에 사용할 이름과 이메일을 입력 (전역 저장소) 
- git config user.name(email) 이름/이메일 : 현재 저장소에서만 사용할 이름과 이메일 입력 (로컬 저장소)
- git config --global --unset user.name(email) : 전역 저장소 이름(이메일) 삭제
- git config --unset user.name(email) : 로컬 저장소 이름(이메일) 삭제
    + 로컬 저장소 이름과 이메일을 삭제해도 전역 저장소에 이름과 이메일이 남아있다면 그 값으로 출력됨
<br>

> **폴더**
- mkdir 폴더 이름 : 폴더 만들기 
- cd 폴더 이름 : 해당 폴더로 이동 
- git init : 폴더를 git repository로 만들기 (그래야 버전 관리 가능)
- cd .. : 해당 폴더를 빠져나와 상위 폴더로 이동 
- cd 폴더 이름 : 해당 폴더로 이동   
