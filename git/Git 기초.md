http://hpy.hk/4ai

1. 깃허브 배쉬 키기ㅎ
   - CLI(command line interface) = 명령줄 인터페이스
   - GUI(Graphic User interface) = 그래픽 유저 인터페이스
   - git bash에 **touch** (예제(CLI.txt)) 치면 새로운 파일이 생겨난다.
   - **ls** 는 리스트를 말한다.
   - **mkdir** git = git이라는 폴더 생성
   - **cd** git => git 폴더에 들어가기
   - **cd ..** => 폴더 뒤로가기
   - **git init** => 저장소를 생성(최초에 한번만)
   - 어떠한 작업을 하고나서
   - **1. 커밋할 목록에 등록**
     **git add .**
   - **2. 커밋**
     **git commit -m 'First commit'** ==> config  오류가 날 시 git config --global user.name (이름) 쓰면 수정됨
   - **3. 버전(이력)**
     **git log**
   - **git config --global -l** => 유저 이메일, 이름 확인 가능
   - **4. 상태**(제일 중요)
     **git status**

----------

# git 기초

> Git은 분산형 버전관리 시스템(DVCS)이다. 

git을 윈도우에서 활용하기 위해서는 [git bash](https://gitforwindows.org/)를 설치해야 한다.


## 1. 저장소 초기화

```bash
$ git init
Initialized empty Git repository in C:/Users/i/Desktop/TIL/.git/

(master) $
```

- 로컬 저장소를 만들고 나면, `.git/`폴더가 생성되고, bash에 `(master)`라고 표기된다.
- 반드시 저장소를 만들기 전에 원하는디렉토리인지 확인하는 습관을 가지고, 저장소 내부에 저장소를 만들지는 말자.
  - 예) Desktop => git 저장소, TIL -> 다른 git 저장소(x)

## 2. add

작업한 내용을 커밋 대상 목록에 추가한다.

```bash
$ add .

# add 명령어 후 상태
$ git status
On branch master

No commits yet
# 커밋이 될 변경 사항들
# working directory X
# Staging area O
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   d2468576cecf1313437de5a883bfa2ed.jpg
        new file:   "markdown-images/\354\272\241\354\262\230-1597900286223.PNG"
        new file:   "markdown-images/\354\272\241\354\262\230.PNG"
        new file:   markdown.md

```



## 3. commit

```bash
$ git commit -m 'Add markdown.cd'
[master (root-commit) 40937b8] Add markdown.cd
 4 files changed, 89 insertions(+)
 create mode 100644 d2468576cecf1313437de5a883bfa2ed.jpg
 create mode 100644 "markdown-images/\354\272\241\354\262\230-1597900286223.PNG"
 create mode 100644 "markdown-images/\354\272\241\354\262\230.PNG"
 create mode 100644 markdown.md

```

- 커밋은 버전(이력)을 기록하는 명령어이다.
- 커밋 메세지는 해당하는 이력을 나타낼 수 있도록 작성하여야 한다. 
- 커밋 이력을 확인하기 위해서는 아래의 명령어를 사용한다.

```bash
$ git log
commit 40937b8941cfdf04da7aec94b9678bc419a20caf (HEAD -> master)
Author: HanHyunDo <guseh147@gmail.com>
Date:   Thu Aug 20 14:58:15 2020 +0900

    Add markdown.cd

$ git log -1
$ git log --oneline
40937b8 (HEAD -> master) Add markdown.cd

$ git log --oneline -1
```

```bash
$ git status
On branch master
# WD X
# Staging area X
nothing to commit, working tree clean
```

