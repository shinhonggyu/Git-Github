
### 세팅하기
[git](https://git-scm.com/downloads)  
[Sourcetree](https://www.sourcetreeapp.com/)  
[iterm2](https://www.iterm2.com/)  
[iTerm셋팅](https://gist.github.com/kevin-smets/8568070)


### 셋업하기 Git config

`git init` 깃초기화 => master branch생성하기  
`ls -al` 숨겨진파일 .git 확인하기  
`open/start` 파일열기  
`rm-rf .git`  git삭제하기  
alias로 단축기설정 


working directory
- untracked (git add 명령어로 트래킹할수있도록 staging area로옮김)  
- tracked - unmodified/modified  

staging area ->commit -> git repository 또는 git directory 라는 git버전히스토리   
git directory의버전들은 checkout으로 원하는버전으로 되돌릴수있다  
git directory ->push -> 서버(remote) -> pull 다시로컬로다운로드

각버전(commit) 해쉬코드를 이용해 버전정보참조

`git rm --cached *` staging area에서 -> 다시 untracked된 working directory

트래킹 하고 싶지 않은 Git과 Github에 올리고싶지않은 파일들은 git ignore파일에 추가할수있다.

어떤 파일의 내용이 수정되었는지 git diff를 통해 확인(working directory만 비교)   
`git diff --staged` 명령어로 staging area에 있는것을 비교   
[diff] tool = vscode / [difftool "vscode"] cmd = code --wait --diff $LOCAL $REMOTE  
git difftool (--staged) 로 vscode에서 확인


`git commit -am "message"`  
add 사용하지 않고 working directory와 staging area 전부커밋

rm 을 이용해서 삭제하면 삭제된 내용은 staging area에 포함되지 않기 때문에 이것을 commit하기위해서는 git add 를이용해 추가해준다음 commit.

git rm 을 이용하면 바로 staging area에 추가된다.  
위와같이 git mv 이용해 파일명 변경후 staging area에 추가

**See History**  
`git log` 커밋리스트  
`git log -p`  각 커밋의 수정된 내용들도 확인할수있다.  
`git log --oneline` 간편하게 확인  
`git log -n` 최근 commit중 n개만 보겠다  
`git show hashcode` 해당하는 특정commit 내용  
••

HEAD는 지금 내가 보고있는 commit을 가리킨다.  
head~1 지금 있는 현재 헤드의 이전 부모 버전을 가르킨다.

`git checkout 각 커밋의 해쉬코드` 를이용해서 원하는시점으로 돌아갈수있다.  
`git checkout master` 로 master branch 첫번째로 다시 돌아오기.  
branch 이동할수있다.

`git log --oneline --graph --all`로 모든 브랜치확인

**git log 꾸미기**  
`git log --pretty` 명령어 로꾸밀수있다.

**git tag**는 특정한 commit을 북마크 해두고싶을때 사용함으로써 내가원하는 부분으로 빠르게 전환 할수있다.  
대부분 v.1.0.0 , v1.0.1 , v2(major).0(minor).0(fix)같이 제품을 릴리즈할때 버전을 많이 tag해둔다.  
`git tag 원하는문자열 해쉬코드 -am ".."`  
`git checkout -b 브랜치이름 태그내용`












