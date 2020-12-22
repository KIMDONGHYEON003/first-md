# git 기초문법

​	git은 분산형 버전관리시스템(DVCS)이다.



## Git 사전 준비

1. 윈도우) [git bash](https://gitforwindows.org/)를 설치한다.
2. 로컬 설정

```bash
$ git config --global user.name 'KIMDONGHYEON'
$ git config --global user.email 'budkim1124@naver.com'
```

* 처음 git을 설치하면, commit을 하는 작성자(author)를 설정해야 한다.

* email 정보는 github에 등록된 이메일을 설정하는 것을 추천 (for 잔디밭)

* 설정된 내용을 확인하기 위해서는 아래의 명령어를 입력한다.

  * ```bash
    $ git config --global -l
    user.email=budkim1124@naver.com
    user.name=KIMDONGHYEON
    ```

  * 오프라인 강의장에서 하는 경우 반드시 체크

    

## 기초흐름

 작업 => add => commit

작업이 끝나면, 커밋할 파일을 모아서(add), 커밋한다.(버전을 기록한다)

### 0. 저장소 설정

```bash
$ git init
Initialized empty Git repository in C:/Users/budki/Desktop/정리용/.git/
(master) $ 
```

* git 저장소로 활용하기 위해서는 위의 명령어를 활용한다.
  * .git 폴더가 생성
  * (master) 로 현재 작업 중인 브랜치 확인



### 1. add

커밋을 위한 파일 목록(staging area)

```bash
$ touch test.txt
```

* add 전 모습

* ```bash
  $ git status
  On branch master
  
  No commits yet
  #트래팅이 되지 않는 파일 : working directory
  Untracked files:
  	# git add 명령어를 사용 !
  	# 커밋이 될 것에 포함시키기 위하여
    (use "git add <file>..." to include in what will be committed)
          test.txt
  # 맨 마지막 줄 : 총정리
  # nothing added to commit : staging area는 아무것도 없다.
  # untracked fils present : WD는 있다.
  nothing added to commit but untracked files present (use "git add" to track)
  
  ```

* add 후 모습

* ```bash
  $ git add .
  $ git status
  On branch master
  
  No commits yet
  # 커밋이 될 변경사항 : SA(staging area) 있다.
  Changes to be committed:
    (use "git rm --cached <file>..." to unstage)
    		# 새파일 : test.txt
          new file:   test.txt
  
  
  ```



### 2. Commit

버전을 기록(스냅샷)

```bash
$ git commit -m '커밋 메시지'
[master (root-commit) a62b06a] test
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt
```

* 커밋 메시지는 현재 작업의 내용을 알 수 있도록 명확하게 작성한다.

* 커밋 이력을 확인하기 위해서는 아래의 명령어를 활용한다.

  * ```bash
    $ git log
    commit a62b06ae747b6774bb7fcb7ee72b491e281ca3f3 (HEAD -> master)
    Author: KIMDONGHYEON <budkim1124@naver.com>
    Date:   Tue Dec 22 14:36:25 2020 +0900
    
        test #커밋 메시지
    
    ```

  * 추가 옵션

    ```bash
    $ git log -1
    $ git log --oneline
    93fff17 (HEAD -> master) 커밋 메시지
    $ git log --oneline -1
    ```

    

### 상태 확인

git 저장소의 현재 상태는 status로 확인하는 습관을 가지자.

```bash
$ git status
```

























