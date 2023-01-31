## 더 쉽게하려면?

  
![image](https://user-images.githubusercontent.com/110442250/215768789-745e1d35-15c7-4cf5-9658-ba22acf79ab0.png)
```
  어지간한 에디터들은 git 기능이 내장되어있음 
  터미널 필요없이 add,commit 가능 
  vscode 기준 + add / v commit 
```

![화면 캡처 2023-01-31 220817](https://user-images.githubusercontent.com/110442250/215768589-d97b5481-9681-4f2e-9dfa-16c83024c1db.jpg)

![image](https://user-images.githubusercontent.com/110442250/215771632-0de5ac20-6ea9-4e96-adf7-0dfb774eaa98.png)

### commmit전에 현재 파일 vs 최근 commit 차이점 확인하는것도 좋다.

```
git diff 
```
최근 commit vs 현재 파일 차이점을 보여준다<br>
하지만 스페이스바 변동사항 등 코드가 길어지면 보기 힘들다<br>
```
git diff 커밋id
```

최근 commit과 비교하는게 아니라 과거의 특정 commit과 현재 파일을 비교하고 싶으면 커밋ID를 명시 <br>
(커밋ID는 git log --oneline 이런거 입력하면 보이는 노란 글자)

```
git diff 커밋id1 커밋id2
```

- 과거의 특정 commit 2개 간의 차이점 비교 

``git difftool 이용하면 조금 더 보기좋음``

- 이거 쓰면 비주얼적으로 훌륭하게 차이점을 분석해줍니다. 

```
  git difftool
```
- 입력하면 현재 파일과 최근 commit의 차이점을 비교해줍니다.
```
  git difftool 커밋id
```
- 입력하면 현재 파일과 특정 commit의 차이점을 비교해줍니다.

```
  git difftool 커밋id1 커밋id2
```

- 입력하면 특정 commit 2개의 차이점을 비교해줍니다.

▲ 이것도 Vim 에디터가 뜨는데 

hjkl 키로 이동가능하고 **:q** 여러번 입력해야 나갈 수 있습니다. 아니면 **:qa** 입력 
※ 편하진 않음

git difftool을 Vim 말고 VSCode로 열고 싶으면 
```
git config --global diff.tool vscode
git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'
```
터미널에 차례로 2개 입력


 




