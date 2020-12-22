## 원격저장소 활용

원격 저장소(remote repository)를 제공하는 서비스는 github, gitlab

, bitbucket 등이 있다.



## 1. 원격저장소 설정하기

```bash
$ git remote add origin (url)
```

* 깃아, 원격저장소를 추가해줘(add) origin 이라는 이름으로 URL을!!

* 원격저장소 설정을 삭제하는  명령어는 다음과 같다.

  ```bash
  $ git remote rm orgin
  ```



## 2. 원격 저장소 확인하기

```bash
$ git remote -v
orgin   https://github.com/KIMDONGHYEON003/project-test/ (fetch)
orgin   https://github.com/KIMDONGHYEON003/project-test/ (push)
origin  https://github.com/KIMDONGHYEON003/project-test.git (fetch)
origin  https://github.com/KIMDONGHYEON003/project-test.git (push)
```



## 3. push

```bash
$ git push orgin master

```

* orgin 저장소의 master 브랜치로 push