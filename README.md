# 협업 테스트

## branch
기존 파일과 상관없이 따로 독립적인 공간을 만들어 파일을 수정할 수 있게 해주는 것이 브랜치 입니다.  
브랜치는 여러개를 만들 수 있고 브랜치 사이를 자유롭게 이동할 수 있습니다.  
Git에서는 브랜치를 만들어 작업을 진행하고 나중에 Merge하는 방식을 권장한다고 합니다.  
Git은 HEAD 라는 포인터가 있는데 HEAD는 지금 작업하는 로컬 브랜치를 가리킵니다.  
브랜치를 새롭게 생성하더라도 HEAD는 자동으로 변경되지 않기 때문에  
checkout 명령어를 통해 브랜치를 이동한 후 작업을 진행해야 합니다.  

브랜치 관련 명령어  
브랜치 생성 : git branch <branch name>  
생성된 브랜치 리스트 확인 : git branch  
브랜치 이동 : git checkout <branch name>  
브랜치 생성 및 이동 한번에 하기 : git -b <branch name>  
브랜치 삭제 : git branch -d <branch name>  
저장소 브랜치 삭제 : git push origin --delete <branch name>  
브랜치 병합 : git merge <병합할 branch name>  

### 병합(merge)
[브랜치와 Merge의 기초](https://git-scm.com/book/ko/v2/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EB%B8%8C%EB%9E%9C%EC%B9%98%EC%99%80-Merge-%EC%9D%98-%EA%B8%B0%EC%B4%88)

## GUI

## 소스트리

## SSH

## 저장소

## 버전관리 / 형상관리

## 명령어

## 병합

## commit message 작성법 정하기