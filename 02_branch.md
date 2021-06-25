# branch command

- 브랜치 생성

  ```bash
  $ git branch {브랜치명}
  ```

- 브랜치 목록

  ```bash
  $ git branch
  ```

- 브랜치 이동

  ```bash
  # git checkout까지만 입력한 상태에서
  # tab*2 -> checkout 가능한 브랜치명 확인 가능
  $ git checkout {브랜치명}
  (브랜치명) $
  ```

  ```bash
  $ git log --oneline
  403956e (HEAD -> master, origin/master, origin/HEAD) update | 00_git_repository.md
  
  ```

  - HEAD : 현재 우리가 속한 위치

  ```bash
  $ git log --all --graph --oneline
  ```

  

- 브랜치 생성 + 이동

  ```bash
  $ git checkout -b {브랜치명}
  ```

- 브랜치 병합

  ```bash
  (master) $ git merge {브랜치명}
  ```

  > 반드시 `master` 브랜치에 `브랜치` 를 병합
  >
  > 1. " I "  ->  --INSERT-- 
  >
  > 2. 수정 (수정하지 않으면 바로 3번으로 이동)
  >
  > 3. ESC 
  >
  > 4. " : wq "
  >
  >    - 수정할 경우 : " I "  ->  INSERT -> 수정 -> Enter
  >
  >    - 수정하지 않을 경우 :  ESC ->" : wq "

  

- 브랜치 삭제

  ```bash
  $ git branch -d {브랜치명}
  ```

- 브랜치 강제 삭제

  ```bash
  $ git branch -D {브랜치명}
  ```

  >  merge가 되지 않은 브랜치는 강제로 삭제해야함
  
  

## 3가지 병합 상황

### 1. fast-forward

"다른 브랜치를 생성한 후, master 브랜치에 변경사항이 없을 때"



### 2. 3-way Merge

"현재 branch(master)가 가리키는 commit이 Merge 할 branch 조상이 아니라면 깃은 현재 브랜치와 머지할 브랜치의 커밋 2개와 두 브랜치의 공통 조상 하나를 사용한다."



#### 1. 새로운 브랜치 signup 생성

#### 2. signup 브랜치에서 signup.py 생성

 - git add, commit 잊지 말기

#### 3. master브랜치에서 new folder와 new.py 파일 생성

	- git add, commit 잊지 말기

#### 4. master 브랜치와 signup 브랜치 삭제

#### 5. signup 브랜치 삭제



###  Merge Confilct

" 두 개의 branch가 동일한 파일의 동일한 위치를 수정하고 merge 하려고 할 때 발생하는 현상

단, 동일 파일을 수정했다고 하더라도 서로 다른 영역을 수정한다면 merge conflict는 발생하지 않는다"

 - git이 자동으로 병합하지 못하는 상황

   

#### 1. 새로운 브랜치 hotfix 생성

```bash
$ git branch hotfix
$ git checkout hotfix
# $ git checkout -b hotfix
```

#### 2. hotfix 브랜치에서 b.txt에 새로운 내용 입력

 - git add , commit

```bash
$ git add . or b.txt
$ git commit -m "message"
```

#### 3. master 브랜치에서 b.txt에 새로운 내용 입력

 - git add , commit

```bash
$ git add . or b.txt
$ git commit -m "message"
```

#### 4. master 브랜치와 hotfix브랜치 병합

```bash
MIJEONG@DESKTOP-0C8DQVU MINGW64 ~/Desktop/github_study (master)
$ git merge hotfix
Auto-merging b.txt
CONFLICT (content): Merge conflict in b.txt
Automatic merge failed; fix conflicts and then commit the result.

MIJEONG@DESKTOP-0C8DQVU MINGW64 ~/Desktop/github_study (master|MERGING)
$
```



