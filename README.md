
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
git diff hashcode hashcode   

#### 버전 삭제 - git reset   
local에서 작업한 내용을 초기화하고싶을때 git reset --hard 버전 

#### 버전을 삭제하지 않으면서 되돌리는 - git revert

#### 히스토리보기 - git log
git hist  
git log -p  
git log --all --graph --oneline  

#### 히스토리가 많아질경우 특정한 커밋을 북마크해두기 - git tag
git tag 문자열 (hashcode)

#### Branch & Merge & Conflict
git checkout -b name
git branch --all (서버포함 보기)  
git branch -d name  
git push origin --delete name (서버 삭제업데이트)  
git branch --move fix fix-welcome (이름 변경)
git push --set-upstream origin fix-welcome (서버 이름변경)
••• 

-----------------------------------------------------------  

(git checkout master-현재branch 로머지) git merge (branch)  
- fast-forward merge  
- git merge --no-ff name
- git이 충돌을 처리하는 방법인 3 way merges

충돌해결 후
- git merge --continue
- git merge --abort(취소)

#### Rebase  
- 3 way merges 에서 히스토리가 남지않게 fast-forward merge 하는방법.  
- branch를 마스터브랜치 최신버전으로 Rebase한다면 fast-forward merge 가능.  
- 서버에 업데이트 되지않은 Local에있는 Commit에만 한함  
(다른 개발자와함께 branch위에서 작업을하고있거나 / 히스토리가 서버에 업로드되있는경우X)   
(내가 Local환경에서 작업을하거나 branch에서 나혼자만 작업하는 경우  
git checkout name
(name) git rebase master  
git checkout master  
git merge name
git branch -d name

브랜치들 사이에서의 Rebase  
(master) git rebase --onto master profile profile-UI 

#### cherry pick (필요한 commit만 쏙)      
(master) git cherry-pick hashcode

#### stash






















