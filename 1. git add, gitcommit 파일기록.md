## 코드 짜다가 2일 전으로 돌아가고싶으면?

  해결 방법은 2가지

 - 매일매일 손수 파일 복사본
 - git 


```
git의 commit 기능을 쓰면 파일의 현재 상태를 매일 기록
원할 때 쉽게 되돌아가거나 그럴 수 있다
```

- *현재 상태를 기록해 줄수 있는 **git commit***


---


작업폴더에서 git 이용하려면?

> 터미널을 연 후 **git init** 설치 

파일 현재 상태를 기록해두려면
> **git add 파일명** <br>
> **git commit -m '메모'**
```
1. git add로 기록할 파일부터 고르고
2. 고른파일 기록명령은 git commit 
```

몰래 어딘가 기록이 됨. 기록이라기 보단 *'버전생성'*




### 용어정리

![image](https://user-images.githubusercontent.com/110442250/215765716-b8244814-5bd9-41f3-a1d8-04bcbed9e296.png)


1. **staging area**는 commit을 하기 전에 commit할 파일들을 골라놓는 곳입니다. <br>
그리고 staging area에 파일넣는 행위를 staging이라고 합니다. <br>
git add 명령어로 staging 할 수 있습니다.<br>

2. **repository**는 commit된 파일의 버전들을 모아놓는 곳입니다. <br>
repository의 실체를 구경하고 싶으면 작업폴더안에 숨겨져 있는 <br>
.git 폴더 열어보면 됩니다. <br>
 **staging area & repository** 2개는 자주 쓰는 용어니까 잘 외우기.<br>


### 또 다른 명령어

  
```
  git add 파일1, 파일2
```
 - 여러파일 동시에 스테이징 가능

```
  git add .
```
- 작업 폴더의 모든 파일을 전부 스테이징 하고싶을때
```
git status
```
- 상태창!!!! 변경된 파일, 스테이징 파일 
- 나 뭐했지? 했을때
```
  git restore --staged 파일명
```
- 스테이징된 파일을 취소하고싶으면 입력
```
  git commit -m '메세지'
```
- commit 할때 -m 메세지 입력가능
- 무슨기능을 추가했는지 요런
```
git log --all --oneline
git log --all --oneline --graph
```
- commit 기록을 한 눈에 파악하고 싶으면 git log 명령어 입력 
- --graph 옵션을 넣으면 그래프로 그려줌 
- vim에디터에선 j,k키로 위아래 스크롤 q키, qa! 종료


---


### 얼마나 자주 commit 하는게 좋음?

ctrl + s 누르는 것 처럼 5초마다 습관적으로 할 이유는 없고 <br>
간단한 기능을 하나 추가할 때 마다 commit 하면 됩니다. <br>

예를 들어 웹개발시 회원가입기능을 만든다고 하면 
- 회원가입 폼 레이아웃을 만들면 commit 
- 입력한 이메일이 맞는지 검증하는 기능을 만들었으면 commit 
- 서버에 전송하는 기능을 만들었으면 commit  
대충 이렇게 작은 작업하나 마쳤으면 commit  <br>
 




