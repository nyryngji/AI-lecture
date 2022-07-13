> **가상환경**
- 원하는 파이썬 환경을 위해 필요한 모듈만 담아놓은 것
- 여러 환경을 만들고 각각의 환경에 여러 버전 설치 가능
<br>

> **명령 프롬프트 pip 점검**
- **where pip** : pip의 위치 출력
- **pip install(<-> uninstall) 패키지명** : 파이썬 환경에 패키지 출력
- **pip list** : 현재 설치된 패키지 출력 
- **pip show 패키지명** : 지정한 패키지 버전 출력
- **pip -h** : 도움말 출력
- **pip -V** : pip버전 확인 
- **python -m pip install --upgrade pip** : pip 업그레이드
- **python -> python -c "문장"** : 파이썬이 잘 실행되는지 테스트
<br>

> **venu 가상환경 생성**
- 1. 가상환경 생성 -> **python -m venv 가상환경 이름**
- 2. 생성된 가상환경 활성화 (들어가기) -> **가상환경 이름\scripts\activate**
- 3. 활성화된 가상환경 내 필요 패키지 설치 -> **pip install 패키지 이름**
- 4. 가상환경 비활성화 (나가기) -> **deactivate**

> **콘다**
- 아나콘다가 제공하는 명령 프롬프트에서 실행되는 명령어 

> **콘다 가상환경 설정** 
- 1. **conda create -n 이름** : 가상환경 만들기
- 2. **conda info -e(=conda env list)** : 현재 가상환경 목록 출력
- 3. **conda activate cnum** : 가상환경 활성화 
- 4. **conda list 패키지 이름** : 패키지 목록 출력
- 5. **conda install python=3.8.13** : 패키지 설치 
- 6. **conda --version** : 현재 콘다 버전 확인 
- 7. **conda uninstall(=remove)** : 설치된 패키지 삭제 
- 8. **conda env remove -n 가상환경 이름** : 가상환경 삭제 
