# Git Command Short Cheatsheet

## Download Git
   
   [Git for windows](https://github.com/git-for-windows/git/releases)

## Git Command

1. Basic
   - clone or download
   
     `git clone <repo url> <customer folder name>`
   
   - save for change
   
     `git commit  <path_to_file> -m " commit message " `
   
   - push to default branch in a remote
   
     `git push origin master`
     
   - pull files from a branch in a remote
     
     `git pull origin master`

1. Version Control
   - get current working branch
   
     `git branch`
   
   - create new branch
   
     `git branch <branchName>`
   
   - switch branch
   
     `git checkout <branchName>`
   
   - create and switch branch in one line
   
     `git checkout -b <newBranch>`
     
   - push to new branch in a remote
     
     `git push origin <branchName>`
   
   - merge a pull request
     see github website
     
   
## Switch accounts for Win
   `control panel` -> `User Accounts` -> `Credential Manager` -> `Web Credentials` -> delete the previous github account
   
   or 
   
   `git config --global --unset-all `
   
   [Useful link](https://stackoverflow.com/questions/28238037/git-log-out-user-from-command-line)
   

## Bash Setting
### 1. Remeber username and password
When pushing, if it repeatedly asks for username and password, you want system to remember your username (or change your username)

`git config [--global] credential.https://github.com.username <your_username>`

or

 `git config [--global] credential.username "new_username"`

`--global` will make it apply globally, or it will only apply to current repo. 

   - To remember username and password: [check here](https://stackoverflow.com/questions/5343068/is-there-a-way-to-skip-password-typing-when-using-https-on-github)

### 2. Mark contributions
To mark your contributions (make your commits associated with your account): identify both your username and email address

  `git config [--global] user.name <username>`
  
  ` git config [-global] user.email <account email address>`
