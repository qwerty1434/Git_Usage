# 깃 사용법
## 참조영상
* https://www.youtube.com/watch?v=lelVripbt2M
* https://www.youtube.com/watch?v=cwC8t9dno2s

## 먼저 git bash를 설치하고 간단한 세팅을 해야 합니다.
* 설치
* ```git config --global user.name "내 이름" ```
* ```git config --global user.email "깃허브 이메일"```
* ```git config --list```를 했을 때 user.name과 user.email이 들어있으면 성공입니다

## 처음 올릴 때
* ```git init``` : 깃을 사용하기 위한 초기화 명령어 입니다. 맨 처음 프로젝트를 올릴 때 ***최초 한 번만*** 해주시면 됩니다.
* ```git add .```: 해당 폴더에 있는 파일을 전부 깃허브에 올리겠다는 뜻입니다.
* ```git status```: 현재상태를 확인하는 것으로, add된 파일이 무엇인지를 확인할 수 있습니다. (업로드와 무관합니다)
* ```git commit -m "first commit"```: 작성 내용에 대한 히스토리를 만들어줍니다.
    * 최종,최종최종,진짜최종,... 같은 느낌입니다 
* ```git remote add origin [git_repository_주소]```: status의 파일을 [git_repository_주소]에 보내겠다는 의미입니다. local과 repository를 연결해 줍니다.
* ```git remote -v```: git repository와 local이 잘 연결되었는지 확인할 수 있습니다. (업로드와 무관합니다)
* ```git push origin master```: 마스터 브랜치에 파일을 올립니다. 최종전송버튼 역할입니다.
## 추가 작업할 때
* ```git add *``` 
* ```git commit -m "second commit"```
* ```origin```에 다른 주소를 덮어쓰지 않았으면 ```git remote add origin [git_repository_주소]```를 생략할 수 있습니다.
* ```git push origin master```


### git을 메일보내기에 비유한다면
```git init```: 메일함을 연다

```git add```: 전송할 파일들을 올린다

```git commit```: 선택을 누른다

```git remote add origin```: 받을사람 주소를 적는다

```git push origin master```: 전송하기 버튼을 누른다


![image](https://user-images.githubusercontent.com/25142537/148748881-0147ec18-502c-45b5-b1d5-5a7572fda379.png)

## 다른사람과 함께 작업할 때
### 개발 참여자
* ```git clone [리퍼지토리 주소] ([폴더이름])```: 로컬에 지금까지의 작업내용을 받아 옵니다.
* 로컬에서 작업을 진행합니다.
* git remote -v를 해서 repository와 git bash가 연결되어 있는지 확인합니다.
	*	연결되어 있지 않다면 git remote add origin <repo주소>를 통해 연결해 줍니다. 	

* ```git add *```: 모든 작업 내용을 업로드 합니다.
* ```git commit -m "contributor\'s first commit"``` 
* ~~git push origin master~~ 마스터에 본인의 코드를 바로 올리면 <font color = 'red'>절대 안됩니다.</font>
* ```git checkout -b [브랜치 이름]```: 본인의 작업을 올릴 브랜치를 생성합니다.
* ```git push origin [브랜치 이름]```: ```master```가 아닌 브랜치에 작업 내용을 올립니다.
*	git repository주소에 접속해 ```compare & pull request```를 누릅니다. // 커밋 메시지 적기,
	* 커밋 메시지를 적어줍니다.
    * ```create pull request```를 누릅니다.(```확인해 보시고 괜찮으면 마스터에 합쳐주세요```라는 의미입니다)

### Repository 생성자 
*	(최초 Repository를 생성합니다)
* [참여자의 pull request 요청이 들어온 후] - branch를 눌러 내용을 확인하고 내용이 괜찮다면 ```merge pull request```를 눌러 ```master```에 합쳐 줍니다.

*	```1.1ver```으로 작업을 하고 있었는데 다른 Contributor가 자신의 작업을 끝내고 이를 ```master```에 추가해 ```1.2ver```이 된 상황을 가정해 봅시다.
	*	생성자는 ```1.2ver```으로의 업데이트도 필요한 동시에 ```1.1ver```의 작업내용이 사라져서는 안됩니다.
	*	먼저 ```1.1ver```에서의 작업을 올려줘야 합니다.
    	*	```git add *```
        *	``` git commit -m "second commit"```
        *	~~git push origin master~~ push 먼저 하면 <font color = 'red'>절대 안됩니다.</font>
		*	``` git pull origin master```:```1.2ver```으로 동기화를 먼저 해 줍니다.
        	*	내 코드와 다른 개발자의 코드 모두 존재하는 상황입니다.
	        *	``` Pulling is not possible because you have unmerged files``` 에러가 뜬다면
		        *	```git commit -am "message"```로 해결 
        *	```git push origin master```로 최종 작업을 ```master```에 올려 줍니다.


## .git ignore
*	Git 버전 관리에서 제외할 파일 목록들

## origin
*	관례적으로 사용하는 변수 이름이다
## branch
* 독립적인 작업이 가능하게 해줌


## 커밋 히스토리 확인
*	git log

## 깃허브 튜토리얼 
*	원숭이 - https://backlog.com/git-tutorial/kr/
*	게임 - https://learngitbranching.js.org/?locale=ko


# Commit Convention
*	https://doublesprogramming.tistory.com/256

# 형상관리
*	소프트웨어의 변경사항을 체계적으로 추적하고 통제하는 것
*	프로젝트와 관련된 모든 변경사항을 관리하는 것

