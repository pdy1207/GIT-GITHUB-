## 코드 맘에안듬 잠깐 삭제할래

```
git stash
```
- 잠깐 다른 공간에 보관됨
- staging 된 것이든 안된것이든 추적중인 파일은 다 이동
- 새로 만든 파일인데 staging 안되어있다면 이동안됨

```
git stash save "코드짯는데 망함 ㅅㄱ"
```
- 메모도 입력가능

```
git stash list
```
- stash 되어있는 코드 목록을 전부 출력해주는 명령어
```
git stash pop
```
- 잠깐 보관했던 코드 불러오기
- git stash 했던 코드가 여러개 있으면 가장 최근에 보관했던 코드부터
- 반대로 가장 최근에 들어온 것 부터 먼저 나감


```
git stash drop 삭제할id
git stash clear
```
- 상단 특정 stash 삭제
- 하단 모든 stash 삭제  <br>
삭제할 아이디? git stash list 하면 보이는 0, 1, 2 넣기

```
git stash -p 
```
- 일부 코드만 git stash 하고싶으면 이거 쓰기
- 그럼 의견물어봄 Y/N

### 주석하자

- 주석처리된 코드는 commit에 반영됨 즉 기록에 남아 더러움
- 주석 처리 내용 commit 하기 싫을때 git stash 쓰면 유용

### 그냥 간단히 브랜치 만들어서 거기 보관하는 것도 나쁘지않음 ㅋㅅㅋ

