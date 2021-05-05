
#### 세팅하기
[git](https://git-scm.com/downloads)  
[Sourcetree](https://www.sourcetreeapp.com/)  
[iterm2](https://www.iterm2.com/)  
[iTerm셋팅](https://gist.github.com/kevin-smets/8568070)

#### git config 설정
vscode 에서 code 명령어 설정 (Command Palette에서 Code검색)
git config --global core.editor "code --wait" 설정

git config --global -e    
[user]      
name = shin     
email = zowoz8819@gmail.com   
[push]    
default = current   
[pull]    
rebase = true   
[core]    
editor = code --wait    
autocrlf = true   
[diff]    
tool = vscode     
[difftool "vscode"]     
cmd = code --wait --diff $LOCAL $REMOTE
[alias]       
hist = log --graph --all --pretty=format:'%C(yellow)[%ad]%C(reset) %C(green)[%h]%C(reset) | %C(white)%s %C(bold red){{%an}}%C(reset) %C(blue)%d%C(reset)' --date=short    
st = status   
[merge]   
tool = p4merge    
[mergetool "vscode"]    
cmd = code --wait $MERGED     
[mergetool]     
keepBackup = false      
[mergetool "p4merge"]     
path = "C:/Program Files/Perforce/p4merge"    
 
---------------------------------------------------------------------     

#### git checkout
- git checkout 해쉬코드 - 특정 버전으로 working tree를 변경 / HEAD 변경  
- git checkout master - 가장최신인 마스터브랜치로 이동
- 브랜치 이동    

#### 어떤 파일의 내용이 수정되었는지 git diff를 통해 확인(working directory만 비교)   
`git diff --staged` 명령어로 staging area에 있는것을 비교   

#### 버전 삭제 - git reset

#### 버전을 삭제하지 않으면서 되돌리기 - git revert

















