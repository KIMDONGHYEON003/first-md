## Gitignore

git으로 관리하지 않을 파일/폴더를 관리

* .gitignore 파일을 생성하여 아래와 같이 작성한다.
  * 메모장에서 편집 금지!

```bash
data.csv #특정 파일
*.png #특정 확장자
secret/ #특정 폴더
!profile.png # 모든 png은 빼고, profile.png는 넣고!
```

* 주의
* OS -WINDOWS/MAC , 개발환경(IDE, text ditor), 특정 언어에서  발생하는 파일/폴더
  * https://gitignore.io
    * 예) 자바로 eclipse로 윈도우에서 개발하고 있다. -> 단어 조합
    * 예) 맥에서 파이썬 주피터 노트북으로 머신러닝을 한다.

