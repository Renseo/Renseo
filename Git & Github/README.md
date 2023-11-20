# Git & Github

## Git 이란?
Linux를 개발하고 있던 Linus Torvalds가 만든 버전 관리 프로그램  
버전 관리 프로그램?  
**버전** - 갤럭시 22, 23 ro 아이폰 14, 15  
**관리** - 시설이나 물건의 유지, 개량 따위의 일을 맡아 함  
**프로그램** - 컴퓨터 프로그램
___
### Git의 버전 관리
한 프로젝트에 대해서 변경점을 기록한다.
- 최초의 원본은 변경점들을 다시 확인하면 알 수 있다.
- 여기에 누가, 언제, 왜 같은 정보를 추가하자.
___
### Git의 분산 버전 관리
**Git**은 분산 버전 관리 프로그램이다.  

분산의 반대를 중앙 집중식
- 하나의 큰 서버에서 전체 프로젝트를 관리
- 개발자는 자기가 수정하고 싶은 부분만
- 수정 완료한 파일을 서버로 보낸다.  

### Git - 서버에서 원본 버전을 저장
- 각각의 개발자도 전체 버전을 저장
- 자신이 기여한 내용을 서버로 전송

### Git과 Github
**Github** - **Git**으로 관리하는 프로젝트를 저장하는 공간을 마련해주는 서비스


## Git 기본기능
### 사전작업
___
**Git**을 설치 후 자신이 누군지를 설정하는 작업  
```
git config --global user.email "tmfcks20@gmail.com"
git config --global user.name "Kim seulchan"
```
`git` - Git을 사용하는 명령어  
`config` - Git 설정 명령어  
`--global` - 프로젝트와 상관없이 이 컴퓨터에 대하여  
`user.eamil` - Git 사용자 email  
`user.name` - Git 사용자 이름
___

### Git으로 버전관리 시작
기본적으로 하나의 풀더가 하나의 프로젝트이다.  
Git을 사용하는 명령은 각 폴더 내부에서 진행할 것.

**Git Bash** 또는 터미널에서, 해당 폴더까지 이동  
`git init` 명령 작성 - 현재 폴더를 **Git**으로 관리하겠다.

`git status` 명령 작성 - 현재 프로젝트의 상태 보기

숨긴 폴더 **.gut**가 생성되어 있다. - **Git** 저장소, **Git**이 관리하고 있는 프로젝트에 대한 정보
___

### 프로젝트에 파일 추가
`README.md`를 만들고, `git status` - 추가 예정파일이 생긴다.  
`git add README.md` 진행 후 다시 `git status`  
`git commit -m "add README.md"` - 프로젝트에 `README.md`가 추가된다
___

### 파일 변경 이력 생성
`README.md` 수정 - `modified:   REAEME.md`  
`git add README.md` - `git commit -m "add README.md"`

Git의 파일 및 변경사항은 세가지 상태를 오간다  
`git add` ------------------------> `git commit` --------------->  
**Git** 에 추가되지 않은 상태 -> **Git** 에 추가 준비 상태 -> **Git** 에 추가된 상태  
<---------------------------------------------------------- 추가 또는 변경
___

### Git에서 파일 제외
`.gitignore`에 포함된 파일은 `Git`에 추가되는 않는다
___
### 작업 이력 (Commit) 확인하기
`git log`
___
## Git 되돌리기
### commit 되지 않은 작업
`README.md` 수정  
`git add` 하기 전 -> `git restore <파일이름>` 으로 되돌릴 수 있다.  
`git add` 진행 이후 -> `git restore --staged <파일이름>` 으로 되돌릴 수 있다.  
___
### commit 되돌리기
`git add` 진행 이후 `commit` 까지 진행  
`commit a023e97` 이 목표 상태
`git reset a023e97`를 진행할 경우 `commit`이 되돌아간다.
___
### Github의 프로젝트 컴퓨터로 가져오기
터미널에서, `git clone <Git주소>`  
파일을 만들고, `add + commit`을 진행할 수 있다.
___
### 컴퓨터의 프로젝트 Github에 올리기
새 프로젝트 만들기  
`git-practice` 폴더 안에서,  
`git remote add origin <Git 주소>`  
`git push --set upstream origin main`
___
### 컴퓨터의 작업내역 Github에 업로드
새로운 `commit` 생성 후, `gut push`  
`git push` - 원격 저장소에 `commit` 업로드
___
### Github의 새로운 이력을 컴퓨터로 가져오기
테스트를 위해 `Github`에서 새로운 파일을 만들어보자.  
`Github`에 연결된 프로젝트 폴더에서 `git pull`
___
### Conflict가 발생할 때
먼저 `Github`에서 파일을 변경해보자. `(commit)`  
컴퓨터에서도 동일한 파일을 변경해보자. `(commit)`  
`git push` 시도  
`rejected` -> 거부되었다. 프로젝트를 관리하는 `Github`에서 거절  
`git pull` 시도  
`CONFLICE: Automatic merge failed;`  
서로 다른 이력(commit)이 같은 파일을 수정하여, 충돌 발생   
위에는 내 컴퓨터, 아래는 `Github`의 내역
1. 충돌이 발생한 파일을 수정해준다.  
내용은 각각의 변경 이유를 살피고 직접 작성해야 한다.
2. `git add`와 `git commit`을 이용해 새로운 `commit`을 생성
3. `CONFLICT`를 해소하는 새로운 `commit`을, 모두 공유하기 위해 `push`  
최종적으로 `Github`에 해당 내용이 반영되었음을 확인한다.