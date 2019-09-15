# Github Basics #

## Github: ##
### Git initialize,file create,add,commit: ###
  * ``` git init ``` To initialize in root directory
  * ``` git status ``` To check current status
  * ``` touch index.html ``` Create index file
  * ``` git add . ``` Add all file/folder within the root project
  * ``` git commit -m ‘message you want to type’ ```
### Git branch operation: ###
  * ``` git branch login ``` Here I am creating a new branch called login
  * ``` git checkout login ``` Moving from existing branch to login branch
  * ``` git checkout -b login ``` Create a branch and move to login branch instantly
  * ``` git checkout master ``` Now I am in master branch
  * ``` git merge login ``` Add login branch with master branch
### Git pull,push to live: ###
  * ``` git pull ``` Download file if any changes made by another developer
  * ``` git clone link ``` Link from online github file , clone the data of a repositories
  * ``` git push --set-upstream origin login ``` Push file on github branch login
  * ``` git push -u origin master ``` Push file on github master
  * ``` git rm -r --cached . ``` Clear cached file..Start again
  * ``` git remote ``` To see origin
  * ``` git remote add origin repisitory_link ``` Repisitory_link from github
### Git Stash (Temporary Storage) ###
  * ``` git stash ``` Create temporary location to save changes file
  * ``` git stash apply ``` Then add stash file on current branch
  * ``` git stash pop ```
  * ``` git stash drop ```
### Git commit history & delete (Temporary Storage) ###
  * ``` git log ``` (To check  commit)
  * ``` git reset --soft HEAD~1 ``` Delete last commit
  * ``` git reset --soft HEAD~2 ``` Delete last two commit
### Git for parent branch ###
  * ```git show-branch | grep '*' | grep -v "$(git rev-parse --abbrev-ref HEAD)" | head -n1 | sed 's/.*\[\(.*\)\].*/\1/' | sed 's/[\^~].*//' ``` Show nearest parent branch
