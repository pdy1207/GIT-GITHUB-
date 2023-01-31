## 프로젝트의 복사본을 만들어서 거기에 먼저 개발을 해보자

  ```
  git branch 브랜치이름
```
- 프로젝트 사본이 생김
- branch? `그냥 프로젝트 복사본`

```
  git switch 브랜치이름
```
- 방금 만든 브랜치로 이동하고싶음
```
  git switch main / master
```
- 다시 메인 브랜치로 되돌아 갈때, 설정에 따라 **main / master**
- 어떤 브랜치지? **git status**


---

> git log? 하면 나오는 HEAD ? <br>
> **현재 위치**

---

### branch 합치기

 ```
원본 코드가 있는 master / main 브랜치에 합치기
```

- 이러한 것을 전문용어로 ***merge***


```
  git switch main
  git merge 브랜치명
```

1. main/master 브랜치로 다시 이동
2. git merge 브랜치명 입력하기 
3. git log --oneline --all --graph 로 확인

### 합칠때 주의사항

master 브랜치와 file브랜치에서 같은 파일, 같은 줄을 수정했을경우 ***merge confilct*** 발생<br>

<br>둘중 어떤 코드를 적용할지 고르면 <br>
<<<< / >>>> / ==== 이런 쓸데없는 것들은 다 지우고 원하는 코드만 남기면 됩니다.

코드를 남길지 정했다?

1. ***git add 파일명***
2. ***git commit -m '메세지'***

### ※ 협업 시 branch 유용!!

기능 하나 추가하고싶어!!

1. ***branch로 프로젝트 사본 만들어서 개발***
2. ***테스트했는데 잘된다 main branch에 합치기***

-> 안정적인 개발


