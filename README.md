
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



















