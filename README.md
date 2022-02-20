# study-python-selenium

### 1. 환경 구성

* python 설치: https://www.python.org/downloads/
  * 파이썬 환경설정 후 CMD를 꼭 껐다 키자..
* Pycharm 사이트 접속: https://www.jetbrains.com/pycharm/download/
  * 파이썬 가상환경 구축 
  * poetry, conda

### 2. 가상환경 세팅 (Mac 환경)
* **poetry** 설치
  ```
  curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
  ```
* poetry가 정상적으로 설치되었는지 확인
  ```
  poetry --version
  ```
* (OSX) poetry 명령어를 찾을 수 없다고 나온다면 다음 명령을 수행한다.
  ```
  * source ~/.bash_profile
  ```
* pycharm에서 poetry 가상환경 추가하기 
  * **[Preferences - 프로젝트의 Python Interpreter - 설정버튼 - Add - Poetry Envireonment]**
  * 또는, command에 
    ```poetry init``` 입력 
  * 성공하게 되면 프로젝트 루트에 <mark>**poetry.lock, pyproject.toml**</mark> 파일이 
* poetry 프로젝트 새로 만들기
  ```
  poetry new [프로젝트 이름] 
  ```

### 3. pyproject.toml
* 생성되었을 때 기본적인 형태 
  ```
  [tool.poetry]
  name = "study-python-selenium"
  version = "0.1.0"
  description = ""
  authors = ["jeonjiyee <jeonjiyee@gmail.com>"]
  
  [tool.poetry.dependencies]
  python = "^3.9"
  
  [tool.poetry.dev-dependencies]
  
  [build-system]
  requires = ["poetry-core>=1.0.0"]
  build-backend = "poetry.core.masonry.api"
  
  ```
* 의존성을 프로젝트에 추가하고 싶다면 tool.poetry.dependencies에 지정해 주면 된다.
* 이때, 파일을 직접 변경할 필요없이 command를 통해 수정 가능 즉, 자동 업데이트를 해준다.
  ```
  poetry add selenium 
  ```


#
###### 유용한 플러그인

- CodeGlance (코드 미니맵)