# CLI

##  ls(list)

- ls 명령어는 현재 작업중인 위치에 존재하는 파일 혹은 폴더 목록을 보여준다

- `백틱 3개는 코드 블락을 생성 할 수 있다.

```bash
MIJEONG@DESKTOP-0C8DQVU MINGW64 ~/Desktop/github_study
$ ls
test_folder/  text.txt

```



## cd(change directory)

- 현재 작업 중인 디렉토리(a.k.a 폴더)를 변경하겠다

```bash
MIJEONG@DESKTOP-0C8DQVU MINGW64 ~
$ cd {directory name}
MIJEONG@DESKTOP-0C8DQVU MINGW64 ~/Desktop/github_study
$ cd .. # 내 상위 폴더로 이동 ( $ cd . -> 내 현재 위치)

```



## pwd

- 현재 작업 중인 디렉토리 표시

```bash
MIJEONG@DESKTOP-0C8DQVU MINGW64 ~/Desktop/github_study
$ pwd
/c/Users/MIJEONG.DESKTOP-0C8DQVU/Desktop/github_study
```



## mkdir(make directory)

- 디렉토리/폴더를 생성한다.

```bash
MIJEONG@DESKTOP-0C8DQVU MINGW64 ~/Desktop/github_study
$ mkdir {directory name}
```



## touch

- 파일을 생성한다.

```bash
MIJEONG@DESKTOP-0C8DQVU MINGW64 ~/Desktop/github_study
$ touch {file name}.{확장자}
```

