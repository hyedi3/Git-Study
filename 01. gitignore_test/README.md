## 🚀  **01. gitignore 실습**
### 🎳 **실습에 사용된 버전**
-  git version : 2.44.0 (2024.04월 기준 맥 최신 깃허브 버전)
<br></br>

### 💻  **Git 최신 버전 설치**
Homebrew 설치 후 아래 명령어를 통해 최신 버전 깃 설치 (맥은 기본적으로 git이 깔려있는데 최신 버전이 아님)
```
brew install git 
```
<br></br>

### 🎱  **Git 최초 설정** 
#### 🎯   Git 전역으로 사용자 이름과 이메일 주소 설정 
- Github 계정 및 원격과는 별개로 터미널 환경에서 설정해줘야 합니다. 
- 터미널 프로그램 (Git Bash, iTerm2)에서 아래 명령어 실행
    ```git
    git config --global user.name " 본인 이름"
    ```
    ```git
    git config --global user.email "본인 이메일"
    ```
<br></br>

#### 🎯  기본 브랜치 명 변경
- GitHub 기본 브랜치는 과거 master로 이루어졌었는데, master라는 단어가 slave와 같이 흑인을 인종차별하는 단어로 구별되면서 현재 GitHub에서도 main 브랜치를 사용하길 권장합니다. 
    ```git
    git config —global init.defaultBranch main
    ```
    > 기본 브랜치로 main을 사용하겠다고 설정하는 코드 

<br></br>

#### 🎯  git repository로 사용할 폴더 초기화 
- git-practice 폴더 생성 후 VS code로 해당 폴더를 엽니다. 해당 폴더의 터미널에 아래 명령어를 입력합니다. 
  ```git
  git init
   ```
  <img src="img/image.png">

    >  .git 폴더 생성  (해당 폴더는 git의 업로드 이력이나 history를 로컬에서 관리하는 폴더로 숨김 처리 되어있습니다.)

<br></br>

### 🎲  **실습용 파일 생성** 
- tigers.yaml 
- lions.yaml 
- secrets.yaml
- .gitignore
<br></br>

### 💻  **변경사항 확인하기**
```git
  git status
```
> 현재 로컬에서 git 관점에서 변경된 사항이 어떤 것들이 있는지 확인할 수 있게 해줍니다. 
<br></br>

### 🎧  **gitignore 형식**
```git
# 모든  file.txt 파일을 무시 
file.txt

# 최상위 폴더의  file.txt 파일을 무시 
/file.txt

#모든 .txt 확장자 파일 무시 
*.txt

# .txt 확장자지만 무시하지 않을 파일
!not_ignore_this.txt

# logs란 이름의 파일 또는 폴더와, 그 내용들 무시
logs

# logs란 이름의 폴더와 그 내용들 무시
logs/

# logs 폴더 바로 안의 debug.log와 .txt 파일 무시 
logs/debug.log
logs/*.txt

# logs 폴더 바로 안, 또는 그 안의 다른 폴더(들) 안의 debug.log 전체 무시 
logs/**/debug.log
```

> https://git-scm.com/docs/gitignore 참조