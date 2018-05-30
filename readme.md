1. 원하는 디렉토리로 이동
```
$ cd go/to/some/directory/here
```
2. 파이썬 3.6이 깔려있는지 확인
```
$ python --version
```
3. `.venv`라 하는 파이썬 가상환경을 만듬
```
$ python -m venv .venv
```
4. 그 가상환경을 활성화
```
$ source .venv/bin/activate
```
5. `requirements.txt`라는 파일에 `ipython`이라 입력
```
$ echo 'ipython' >> requirements.txt
```
6. `requirements.txt` 내용 확인
```
$ cat requirements.txt
```
7. 패키지 매니저 (`pip`) 이용하여 `requirements.txt`에 표기된 패키지를 설치
```
$ pip install -r requirements.txt
```
8. 알파벳 순서대로 가상환경에 설치된 패키지들을 나열
```
$ pip freeze | sort
```
9. 가상환경에 설치된 `ipython`을 실행
```
$ ipython
```
10. 날코딩의 시작