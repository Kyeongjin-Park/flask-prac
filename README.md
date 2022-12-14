# 폴더, 파일 생성
```
learn-flask<br/>
├── main.py<br/>
└── website<br/>
    ├── __init__.py<br/>
    ├── auth.py<br/>
    ├── models.py<br/>
    ├── static<br/>
    ├── templates<br/>
    └── views.py<br/>
```
---
# 폴더 파일 설명
- `website` : 구현할 웹 사이트의 모든 코드가 저장<br/>
- `main.py` : 웹 서버가 시작(run)시키는 코드<br/>
- `static templates` : 웹 페이지를 구성하는 파일(html, css, js)들을 놓아두고 서버가 활용하도록 합니다.<br/>
- `__init__.py` : website 폴더를 웹 사이트 관련 폴더로 인식시키기 위해서 생성. 패키지화.<br/>
- `auth.py` : 로그인처럼 인증과 관련된 기능을 구현할 곳<br/>
- `models.py` : 웹 사이트에서 다뤄지는 데이터의 구조. 즉 데이터베이스 모델을 구현할 곳. Database와 관련됩니다.<br/>
- `views.py` : 클라이언트가 요청해서 서버가 웹 사이트를 보여주기위해 응답하는 과정의 모든 데이터의 요청과 응답을 관여합니다.<br/>
  - View라고 프론트엔드 느낌의 View를 생각하면 오해의 소지가 있다.<br/>
  - Spring프레임워크의 Controller에 해당.<br/>
- Django를 경험해봤다면 구조가 유사하다고 생각할 듯.<br/>
---
# 가상환경 세팅
- `learn-flask` 위치애서 가상환경을 생성하고 필요한 모듈을 설치해봅시다.
- 터미널을 열어 해당 위치에 flask를 위한 가상환경을 세팅합니다.
- pipenv가 없다면 설치하고 진행합니다.
  - `pip3 install pipenv`
- flask를 위한 가상환경을 생성합니다.
  - `pipenv install flask` 
  - `pipenv install flask-login` 
  - `pipenv install flask-sqlalchemy`
---
# 가상 환경 진입
- `pipenv shell`
- `pip3 list`를 입력하여 나오는 출력에 아래 3개가 있는 지 확인합시다.
- `Flask`, `Flask-Login`, `Flask-SQLAlchemy`
- 위 3개에서 없는 것이 있다면 설치하자.
  - `pip install flask`
  - `pip install flask-login`
  - `pip install flask-sqlalchemy`
---
# VScode에서 Python 인터프리터 경로 변경하기
- 터미널에 가상환경 들어간다고 VSCode 에디터에서 인식한 파이썬이 달라지진 않는다.
<br/>
<br/>
- 인터프리터 경로 변경

1. 명령 팔레트(Ctrl+Shift+P, Command+Shift+P)를 열어 Python3 인터프리터를 선택합니다.
2. Python: Select interpreter를 입력
3. 경로에 virtualenv\ 가 들어간 python 을 선택. 우측에 PipEnv라고 뜰 것
4. 터미널에서 Python Debug Console을 삭제 후 다시 실행해보면 성공