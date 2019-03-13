# 협업 테스트

## branch
- 기존 파일과 상관없이 따로 독립적인 공간을 만들어 파일을 수정할 수 있게 해주는 것이 브랜치 입니다."
- 브랜치는 여러개를 만들 수 있고 브랜치 사이를 자유롭게 이동할 수 있습니다.
- Git에서는 브랜치를 만들어 작업을 진행하고 나중에 Merge하는 방식을 권장한다고 합니다.
- Git은 HEAD 라는 포인터가 있는데 HEAD는 지금 작업하는 로컬 브랜치를 가리킵니다.
- 브랜치를 새롭게 생성하더라도 HEAD는 자동으로 변경되지 않기 때문에
- checkout 명령어를 통해 브랜치를 이동한 후 작업을 진행해야 합니다.

### 브랜치 관련 명령어
- 브랜치 생성 : `git branch <branch name>`
- 생성된 브랜치 리스트 확인 : `git branch`
- 브랜치 이동 : `git checkout <branch name>`
- 브랜치 생성 및 이동 한번에 하기 : `git -b <branch name>`
- 브랜치 삭제 : `git branch -d <branch name>`
- 저장소 브랜치 삭제 : `git push origin --delete <branch name>`
- 브랜치 병합 : `git merge <병합할 branch name>`

### 브랜치 네이밍

|name|feat|
|---|---|
wip|곧 끝나지 않을 진행중인 작업
feat|기능 추가 또는 확장 중
bug|버그 수정 또는 실험
junk|테스트

- 지점 이름 앞에 "그룹화" 토큰을 사용하십시오.
내맘대로 수정_jhy
```
dfdfadfadfadfadf
group1/foo
group2/foo
group1/bar
group2/bar
group3/bar
group1/baz
```
* testdfsdfdsaf
### 병합(merge)
[브랜치와 Merge의 기초] (https://git-scm.com/book/ko/v2/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EB%B8%8C%EB%9E%9C%EC%B9%98%EC%99%80-Merge-%EC%9D%98-%EA%B8%B0%EC%B4%88)

## GUI

## 소스트리

※Sourcetree 설치 방법 참고 url : https://hackersstudy.tistory.com/41
※Sourcetree download 사이트 url: https://www.sourcetreeapp.com/
※git client 관련한 장단점 url : https://www.lesstif.com/pages/viewpage.action?pageId=20774956


1. msysgit
- [장점]
  Windows에 포팅된 git 으로 POSIX 호환 레이어에서 도는 cygwin 에 내장된 git 보다 안정적. OS 가 Windows 라면 유일한 대안.
- [단점]
  cmd 방식이라 사용이 너무 어려움.

2. SmartGit
- [장점]
  Java 로 개발되어 Multi platform 지원 (내부적으로는 git command 사용하므로 msysgit 필요)
- [단점]
  1) UI 가 직관적이지 못 하고 사용이 어려움(기본적으로 변경되지 않은 파일은 목록에 안 보여서 로그 보는데 애를 먹음)
  2) 기업에서 사용하려면 비용 발생
3. TortoiseGit
- [장점] 익숙한 TortoiseSVN 의 소스를 기반으로 개발되어 기존 Tortoise 사용자라면 UI 가 친숙함
- [단점] 1) 기능 및 안정성이 부족함.
  2) Mac 용 없음.
4. github client for Windows/Mac
- [장점] github 가 배포하는 클라이언트로 github 사용시 유용함.
- [단점] 기능이 아직 부실함.


※ Sourcetree 설치 및 commit 방법

1. https://www.sourcetreeapp.com (소스트리 : gui 환경에서 git을 사용할 수 있게하는 프로그램) 접속하여 소스트리를 다운받는다.

2. 왼쪽 상단에 파일 - new 탭을 클릭 -> create 저장소를 만들어준다. (로컬 경로 지정, 이름 지정, 생성)

3. 지정된 폴더에 임시 text 파일을 생성한다.
![img1](https://user-images.githubusercontent.com/46946241/53864998-4bc09c00-4031-11e9-8ef9-13ca6c222b67.jpg)

4. 스테이지에 올라가지 않은 파일에 있는 파일을 log와 함께 커밋한다.
![img2](https://user-images.githubusercontent.com/46946241/53865021-5f6c0280-4031-11e9-91ab-5632c74d5fe1.jpg)

5. 커밋하면 스테이지에 올라간 파일 목록에 뜨며, 추가되거나, 수정된 부분이 표시된다.
![img3](https://user-images.githubusercontent.com/46946241/53865023-61ce5c80-4031-11e9-904d-d2fffe20419e.jpg)

6. 수정 후 커밋하지 않으면 커밋하지 않은 변경사항 목록에 뜬다.
![img4](https://user-images.githubusercontent.com/46946241/53865028-63982000-4031-11e9-9c89-89c9343eaf39.jpg)

7. 최종 수정된 파일을 github에 올리기 위해, 저장소 -> 저장소 설정에서 내 github url을 추가한다.
![img5](https://user-images.githubusercontent.com/46946241/53865034-66931080-4031-11e9-9457-a7dc3f2bd815.jpg)

8. 추가된 저장소에 push한다.
![img7](https://user-images.githubusercontent.com/46946241/53865037-68f56a80-4031-11e9-983f-f00dcc6d6bea.jpg)

9. github 로그인을 안하면, 로그인 하라고 뜬다.
![img8](https://user-images.githubusercontent.com/46946241/53865044-6a269780-4031-11e9-8736-a756d7d52304.jpg)

10. 모든 branch 목록이 뜬다.
![img9](https://user-images.githubusercontent.com/46946241/53865046-6bf05b00-4031-11e9-9c6f-70eb74f1292e.jpg)

11. 결과 화면 및 수정했던 로그도 같이 뜬다. (https://github.com/heayun/ex1)
![img10](https://user-images.githubusercontent.com/46946241/53865047-6d218800-4031-11e9-94c8-4cb56e7c25ca.jpg)
![img11](https://user-images.githubusercontent.com/46946241/53865048-6eeb4b80-4031-11e9-9a9a-1328b26dcf27.jpg)
![img12](https://user-images.githubusercontent.com/46946241/53865050-701c7880-4031-11e9-84b9-b7d280b7b104.jpg)


## SSH

## 저장소

## 버전관리 / 형상관리

## 명령어

## 병합

## commit message 작성법 정하기

### Git 명령어1(git 기본 명령어)

#### commit(git commit)
git저장소에 내 디렉토리에 있는 모든 파일에 대한 스탭샷을 기록하는 것. 디렉토리 전체를 복사해서 붙여넣는것보다 유용.
커밋할 때마다 저장소의 이전버전과 다음 버전의 변경 내역("delta")을 저장.
:: 커밋을 할 때마다 부모커밋을 기반으로 변경되어 새로운 커밋 생성


#### branch(git branch 브랜치명)
특정 커밋에 대한 참조(reference).
하나의 커밋과 그 부모 커밋들을 포함하는 작업 내역
:: branch를 만든 시점의 커밋을 가리킨다.
:: master branch에 있는 상태에서 new branch생성 후 commit을 하게 되면 new branch는 생성 커밋 시점에 머물면서 master branch가 다음 커밋으로.


#### checkout(git checkout 브랜치명)
새 브랜치로 이동.
:: 새 브랜치에 커밋하고 싶을때 checkout으로 브랜치를 이동한 다음 commit


#### merge(git merge 브랜치명)
두 별도의 브렌치를 합치는 방법 1
두개의 부모를 가리키는 커밋(한 부모의 모든 작업내역과 나머지 부모의 모든 작업, 두 부모의 모든 부모들의 작업내역을 포함한다.)
:: 2개의 브랜치에 각각 독립된 커밋이 하나씩 있어 작업 내역이 나뉘어 담겨있는 경우.
:: ex)) a브랜치를 master에 merge하고 a브랜치로 이동 후 master 브랜치를 merge하면 두개의 브랜치가 모든 부모의 작업 내역을 포함


#### rebase(git rebase 브랜치명)
두 별도의 브렌치를 합치는 방법 2
커밋들을 모아서 복사한 뒤, 다른 곳에 떨궈 놓는 방법.
커밋들의 흐름을 보기 좋게 한줄로 만들 수 있다는 장점이 있어 저장소의 커밋로그와 이력이 깔끔하다.
: 나뉘어져 있는 브랜치를 해당 브랜치 위 쪽으로 복사해서 붙여넣고 해당 브랜치를 붙여넣은 브랜치로 이동시켜 한 줄로 이력을 만들어준다.




### Git 명령어2(프로젝트를 표현하는 커밋 트리(commit tree)에서 이동 할 수 있는 방법)

#### HEAD
현재 체크아웃 된 커밋(현재 작업 중인 커밋) === 작업 트리의 가장 최근 커밋으로 작업 트리에 변화를 주는 명령어들은 대부분 HEAD변경으로 부터 시작.
HEAD는 브랜치의 이름을 가리키고, 커밋 후 변경내용은 HEAD를 통해 확인 가능.

##### HEAD분리(git checkout commit1)
각 커밋은 해당 커밋의 해시값(label)으로 특정지을 수 있음.(__git log__ 로 해시 확인 가능 / 긴 해시의 고유값임을 보여줄 수 있을만큼 명시하면 된다.)
HEAD 분리 전 : HEAD -> master -> commit1 / 분리 후 : HEAD -> commit1


#### 상대참조(relative refs)
브랜치 혹은 HEAD 등에서 출발해서 이동해 다른 지점에 도달해 작업 가능

**-한번에 한 커밋 위로 움직이는 ^**
: 참조 이름에 하나씩 추가할때마다 해당 커밋의 부모를 찾음
: ex) master^ , master^^

**-한번에 여러 커밋 위로 올라가는 ~숫자**
: 선택적으로 올라가고 싶은 부모의 개
: ex) git checkout HEAD~4

_※브랜치 강제로 옮기기(상대참조를 사용하는 가장 일반적인 방법)_
__git branch -f master HEAD~3__ ex)강제로 master 브랜치를 HEAD에서 세번 뒤로 옮김
: 브랜치 강제 -f



### Git 명령어3(git에서 작업 되돌리기)

#### reset(git reset HEAD~1)
브랜치가 예전의 커밋을 가리키도록 이동시키는 방식(히스토리를 고쳐씀) == 커밋하지 않은것처럼 예전 커밋으로 브랜치를 옮기는 작업
: 로컬브랜치에서는 가능하지만 리모트 브랜치에서는 불가능


#### revert(git revert HEAD)
: 되돌리려고 한 커밋의 아래에 새로운 커밋이 생기고 생긴 커밋에 변경내용이 기록됨.
revert 후 다른사람에게도 변경내역을 push할 수 있음.



### Git 명령어3(작업 여기저기로 옮기기)

#### cherry-pick(git cherry-pick <commit1> <commit2> <...>)
현 위치(HEAD)아래에 있는 일련의 커밋들에 대한 복사본을 만듬.
: 브랜치에 있는 일부 커밋들만 따로 빼서 다른 브랜치에 병합가능
: 해당 커밋과 각 커밋의 해시값을 알 때 유용


#### interactive Rebase(git rebase -i HEAD~3)
rebase명령어 사용 + -i옵션의 개념
: 리베이스의 목적지가 되는 곳 아래에 복사될 커밋들을 보여주는 파일이 편집기에서 열림.
1. 적용할 커밋의 순서 변경
2. 원하지 않는 커밋을 제외(pick을 이용해 지정)
3. 커밋을 스쿼시(squash), 즉 커밋을 합침



### Git 명령어4(개발 상황에 따른 원하는 커밋 가져오기)

#### 디버깅용 코드를 제외한 나머지 브랜치 내용을 master브랜치에 합치고 싶을때
__**git rebase -i**__ : 커밋의 순서, 일부 커밋의 삭제 등 선택 가능
__**git cheery-pick**__ :개별 커밋을 골라서 HEAD위에 떨어뜨리기 가능


#### 2개의 다른 브랜치에서 각각의 변경내역이 있는 상태에서 이전 커밋의 내용을 일부 변경하는 경우

##### rebase -i방법
1. __git rebase -i__ : 바꿀 커밋을 가장 최근 순서로 변경
2. __git commit --amend__ : 커밋 내용 정정
3. __git rebase -i__ : 이전 커밋을 그 자리로 되돌려 놓기
4. master를 지금 트리가 변경된 부분으로 이동
:: 순서를 많이 바궈야 해서 리베이스 중에 충돌이 날 우려가 있음.

##### cherry-pick방법
1. __git checkout 브랜치명__: 브랜치를 분리할 위치로 이동
2. __git cherry-pick hash명__ : 해당 커밋 복사
3. __git commit --amend__ : 해당 커밋 내용 정정
4. __git cherry-pick hash명__ : 최근 커밋 복사


#### history의 중요 지점들 영구적인 방법(git tag 태그이름 커밋해시명or브랜치명)
특정 커밋들을 브랜치로 참조하듯 영구적인 이정표(milestone)lev로 표시
:Git태그는 커밋이 추가적으로 생성되어도 절대로 움직이지 않음.
  == 태그를 checkout한 후에 그 태그에서 어떤 작업을 완료할 수 없음.(태그에 체크아웃 할 시 head를 분리함)
:커밋을 지정해 주지 않으면 HEAD가 있는 지점에 태그를 붙임


#### 커밋히스토리에서 여러 커밋을 이동 한 후 방향감각을 찾을때(git describe 커밋해쉬명)
가장 가까운 tag에 비해 상대적으로 어디에 위치해있는지 묘사(describe)해주는 명렁어.
:커밋을 지정해 주지 않으면 지금 checkout되어 있는 곳을 사용(HEAD)
__메시지 형태 : 가장가까운 부모tag_그태그가 몇 커밋 멀리 있는지_g묘사하고 있는 현재 커밋의 해시__



### Git 명령어5(기타)

#### 부모선택하기(git checkout 브랜치명^숫자)
~ 수식 : 몇개의 세대를 돌아갈지 결정 / ^ 수식 : 병합이 된 커밋에서 어떤 부모를 참조할 지 선택
보통 병합된 커밋에서 첫 부모를 따라가지만 ^ 수식 + 숫자를 사용할 경우 숫자만큼의 부모를 찾아감.
: ~ 수식과 ^ 수식을 한 명령어에 병행해서 쓸 수 있다.(git checkout HEAD~^2~2)


### Git 명령어6(유용한 명령어)

- 최근 커밋 취소
```
git reset HEAD^
```

- 최근 수정 사항 삭제
```
git checkout <file name>
```

- branch 병합하기
```
git checkout <병합 베이스 branch>
git merge <병합하고 싶은 내용이 있는 branch>
```
> <병합하고 싶은 내용이 있는 branch> 소스를 <병합 베이스 branch> 에 추가 한다.



### 원격저장소
원격 저장소 == 또 하나의 컴퓨터에 있는 내 저장소의 복사본
- 원격저장소의 장점
+ 백업으로서의 역할(로컬저장소의 파일을 이전상태로 되돌리거나 정보를 잃더라도 복사본으로 버전을 다시 관리 할 수 있음)
+ 다른 사람과의 협업 가능
- 원격저장소 시각화 프로그램
+ github, phabricator



#### clone__(git clone)__
원격저장소의 복사본을 로컬에 생성하면 로컬에 원격 브랜치가 생성

##### 원격 브랜치
__★ 원격저장소의 상태를 반영__
네임규칙(remote name:원격저장소이름/branch name) -> 보통 원격저장소를 origin이라고 짓는다
-체크아웃을 게 되면 분리된 HEAD모드로 가게 되는 속성을 가지고 있음.(이 브랜치들에서 직접 작업할 수 없기 때문)
-origin/master는 새로운 커밋을 추가해도 갱신하지 않는다.(원격저장소가 갱신 될 때만 갱신)



#### fetch(git fetch)
원격저장소에서 데이터를 가져오는 방법(다운로드 개념)
원격저장소와 작업을 해서 상태가 변할 경우 원격 브랜치들도 그 변경을 반영
(원격저장소에 변화가 있으면 현재 내 브랜치는 그대로 있고 origin/master가 그 변경상태를 적용해서 변하게 됨)
1. 원격저장소에는 있지만 로컬에 없는 커밋을 다운로드
2. 원격브랜치가 가리키는 곳 업데이트
3. 결국 로컬에서 나타내는 원격 저장소의 상태를 실제 원격 저장소의 현재 상태와 __동기화__
4. 인터넷을 통해 접근(http:// or git://과 같은 프로토콜로)
5. __로컬파일이나 로컬브랜치를 변경하지 않음__


#### pull(git pull)
작업을 업데이트 하고 변경을 반영하는 작업.(원격저장소의 변경을 fetch하고 merge하는 작업)


#### fakeTeamwork(git fakeTeamwork /추가 할 브랜치 갯수 /)
원격 master에 간단히 하나의 커밋을 한 것 처럼 가장의 커밋


#### push(git push)



## 병합

## git 협업 과정

1. Fork
1. clone, remote설정
1. branch 생성
1. 수정 작업 후 add, commit, push
1. Pull Request 생성(GitHub 기능)
1. 코드리뷰, Merge Pull Reqest
1. Merge 이후 branch 삭제 및 동기화

### Q1) 로컬 브랜치에서 작업 중인 경우, 원본 프로젝트의 sync는 언제? 어떻게?
» 협업의 경우, PR이 Merge되면 각자 자신의 로컬 master에 해당 내용을 자주 반영하는게 좋음<br>
» 내가 작업중인 브랜치는 git rebase master를 통해서 그래프 최상단으로 올리는 것이 히스토리 관리가 깔끔해짐