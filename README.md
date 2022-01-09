# 깃 사용법
* git bash 설치
* git bash 세팅
  * git config --global user.name "내 이름" 
  * git config --global user.email "깃허브 이메일"
  * config 확인 : git config --list
## 최초
* git init // 깃을 사용하기 위해 초기화를 하겠다, `맨처음` 프로젝트를 올릴 때 git init을 해줘야 함 (처음 한번만)
* git add . // 해당 폴더에 있는 파일 전부 다 깃헙에 올리기
* git status // 현재상태, add될 파일이 무엇인지를 보여줌, (필수 아님)
* git commit -m "first commit" // git commit: 히스토리를 만들어줌, 최종(first commit),최종최종,진짜최종,...같은 느낌 (커밋 메시지가 히스토리 이름)
* git remote add origin [git repository주소] // status의 파일을 [git repository주소]에 보내겠다는 뜻, repository와 local를 연결
* git remote -v // git repository와 local이 잘 연결되었는지 확인할 수 있음
* git push origin master // 전송버튼
## 수정
* git add * 
* git commit -m "second commit"
* 배쉬를 껐다가 켰을 때 git remote add origin [주소] 는 안해도 되는건가?
* git push origin master


## 사용하던 것
* (git init)
* git add [filename]
* git commit -m [commit message]
* git remote add origin [개인git주소]
* (git remote remove origin // orogin 삭제
* git push origin master




## .git ignore는 무슨 역할을 하는가


## origin이란?

## branch란?

## 다른사람과 깃헙으로 협업하려면?

https://backlog.com/git-tutorial/kr/
