## 원격 repository 개념과 왜 사용하는가?

### ***repository란?***
> 한국말론 **저장소**  <br>
> 실제로 개발할땐 온라인 repository 많이 사용 <br>
**내가 컴퓨터에 만들어 놓은 저장소를 온라인으로 저장해두는것**
---
> 다른사람과의 **협업** 가능


1. github repostitory 하나 만들기
2. 원격저장소 만들기  <br>
    2-1. 원격 저장소 쓰는이유? **내 컴퓨터에 만들어둔 저장소를 백업하기위함** 

3. `git init` 저장소 만들기 <br>
    3-1. **로컬 리포지토리 생성법**

4. 기본 브랜치 이름 설정 

```
git branch -M main
```
- 너의 이름은 master 가 아니라 main임

### github에서 만든 원격 저장소에 올리기

- 로컬 저장소 -> 원격 저장소

 ```
  이렇게 업로드 하고 싶으면 터미널 키고 
  git pusho -u 원격저장소주소 main
```
- 로컬저장소의 main 브랜치를 원격저장소에 올리라는 뜻 / 다른 브랜치도 가능
- -u 옵션은 입력한 주소 기억해두라는 뜻 
- 한번만 해도 그 후 git push만 해도 잘됨
- 다음부터는 git push만 입력해도 잘됨

![image](https://user-images.githubusercontent.com/110442250/215792200-dfa599ea-569c-4ee8-8a3e-4beed1f3f639.png)


## 원격저장소주소 길게 입력하는게 귀찮아

```
  git remote add origin https://github.com/pdy1207/app.git
```
- git remote add 변수명 저장소 주소
- git remote -v 변수목록 살펴보기

## 원격저장소 그대로 내려받기
```
git clone https://원격저장소주소
```
- 고대로 내려받기


### 저장소에 올리지 않은 파일들은 .gitignore

- 원격저장소 **효율적으로 쓰고 싶으면 쓸대 없는 파일은 commit해서 올리지 않는게 좋음**
- .gitignore 저장소에 올리지 않을 파일들을 **쉽게 명시가능**
- 명시한 파일은 git add . 해도 스테이징 안됨

> 웹 개발 예를 들면 node_modules 이런폴더 안올림 <br>
 package.json파일만 잘 있으면 npm install 입력하면 자동 node_modules 폴더생성






