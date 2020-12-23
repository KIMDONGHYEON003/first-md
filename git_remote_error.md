## 원격저장소 push시 오류

```bash
$ git push origin master
To https://github.com/KIMDONGHYEON003/first-md.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/KIMDONGHYEON003/first-md.git'
# 거절됨 (rejected)
# 원격 저장소의 작업이 로컬에 없음.
hint: Updates were rejected because the remote contains work that you do
# 다른 저장소에 push하는 경우도 발생 가능
hint: not have locally. This is usually caused by another repository pushing
# 너는 원할거다..
# 원격 저장소의 변경사항을 먼저 통합하고
# git pull ...
hint: to the same ref. You may want to first integrate the remote changes
# 다시 push
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```

* 원격 저장소와 로컬 저장소의 커밋 히스토리를 확인

  ```bash
  $ git pull origin master
  remote: Enumerating objects: 4, done.
  remote: Counting objects: 100% (4/4), done.
  remote: Compressing objects: 100% (2/2), done.
  remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
  Unpacking objects: 100% (3/3), 683 bytes | 14.00 KiB/s, done.
  From https://github.com/KIMDONGHYEON003/first-md
   * branch            master     -> FETCH_HEAD
     b4cc452..1c7c648  master     -> origin/master
  Merge made by the 'recursive' strategy.
   README_1.md | 2 ++
   1 file changed, 2 insertions(+)
   create mode 100644 README_1.md
  ```

  * vim 편집기 창이 popup 될건,
    * esc + :wq 엔터
      * w : write(저장)
      * q : quit (나가기)

* log 를 확인하나.

  ```bash
  $ git log --oneline
  # vim 편집기가 뜬 이유 -> 합쳐졌다는 사실을 커밋으로 남김
  913988e (HEAD -> master) Merge branch 'master' of https://github.com/KIMDONGHYEON003/first-md
  # 로컬 작업한 것
  752b70b Add test
  # 원격 저장소에서 작업한 것
  1c7c648 (origin/master) Create README_1.md
  a5d05a2 (orgin/master) first-md
  b4cc452 First-md
  ```

* 다시 push 한다.

  ```bash
  $ git push origin master
  Enumerating objects: 9, done.
  Counting objects: 100% (8/8), done.
  Delta compression using up to 4 threads
  Compressing objects: 100% (5/5), done.
  Writing objects: 100% (5/5), 560 bytes | 280.00 KiB/s, done.
  Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
  remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
  To https://github.com/KIMDONGHYEON003/first-md.git
     1c7c648..913988e  master -> master
  ```

  