# Git Gui

 Alternative to the command line

[GitKaren](https://support.gitkraken.com/how-to-install): beautiful GUI 

[SourceTree](https://www.sourcetreeapp.com/): Free enterprise-grade tool

# Set up
## 1. Download

SourceTree could be downloaded from the link above. It would need some time (SourceTree made me download .Net first and it was a long process). 

## 2. Setup
Setting up requires login and you could registrate an account at that page. 

## 3. Connect GitHub to SourceTree
`Tools`->`option`->`Authentication`->`Add (under Account panel)`, then choose `GitHub` as the Hosting Service, then click `Refresh Oauth Token` and click accpet.

# General command
# 1. Clone
`Source Path`: github repo url
`Destination Path`: the local folder path. This folder should either be empty or don't exist (after cloning, the folder will be created). 

# 2. Commit 
Under the working repo, choose the branch you want to commit. 
  - Click `Commit` at the top left corner. 
  - All the new or changed files will be showed in `Unstaged files`.
  - Select the files you want to commit, then click `Stage Selected` (or  `Stage All`)
  - Add comment and then click `Commit`.
  
# 3. Push
The number showed in the `Push` button means the number of commits the local repo is ahead of the remote repo.
Simply click `push`.

# 4. Pull
click `Pull`.

# 5. Branch and Merge
Manage branches by clicking `Branch`, creating or deleting branch. 
Merge is similar. Click `Merge`.




