# Git Basics #

## Git: ##

### Git install: ###
  * ``` sudo apt-get update ``` System update
  * ``` sudo apt-get install git-all ``` Git install
  * ``` sudo apt-get install git-gui ``` Git gui install
  
### SSH key generate and configure: ###
  * ``` ssh-keygen -t rsa ``` or ``` ssh-keygen -t rsa -b 4096 -C "your github repo ssh" ``` Generate SSH key
  * ``` eval "$(ssh-agent -s)" ```
  * ``` ssh-add ~/.ssh/id_rsa ```
  * Go to local ssh directory copy public key to github setting -> ssh-keys
  * ``` git clone your_github_repo_ssh ```
  
   #### If you will face "Unable to negotiate" or "Cipher key" related problem: ####
  
   * ``` sudo vi /etc/ssh/ssh_config  ``` It will open an comand line editor
       * Press I for insert or edit
       * Copy ``` Ciphers aes128-ctr,aes192-ctr,aes256-ctr,aes128-cbc,3des-cbc ```
       * Press ``` shift + : ``` 
       * Then type "wq" & press enter ( w = write & q = quit ) Changes will be saved
   * Or you can just simply open ssh_config file, write ``` Ciphers aes128-ctr,aes192-ctr,aes256-ctr,aes128-cbc,3des-cbc ``` & save then exit

### Git initialize,file create,add,commit: ###
  * ``` git config --global user.name "Mazhar Hossain" ``` Add username
  * ``` git config --global user.email "github email" ``` Add email address
  * ``` git init ``` To initialize in root directory
  * ``` git status ``` To check current status
  * ``` touch index.html ``` Create index file
  * ``` git add index.html ``` Add single file in a project
  * ``` git add . ``` Add all file/folder in a project
  * ``` git reset filename ``` Move file from staging area to working directory
  * ``` git commit -m "message you want to type" ```
  * ``` git clone link ``` Link from online github file , clone the data of a repositories
### Git branch operation: ###
  * ``` git branch login ``` Here I am creating a new branch called login
  * ``` git checkout login ``` Moving from existing branch to login branch
  * ``` git checkout -b login ``` Create a branch and move to login branch instantly
  * ``` git checkout master ``` Now I am in master branch
  * ``` git merge login ``` Add login branch with current branch ( Use git status to check your current branch )
### Git pull,push to live: ###
  * ``` git pull ``` Download file if any changes made by another developer
  * ``` git push --set-upstream origin login ``` Push file on github branch login
  * ``` git push -u origin master ``` Push file on github master
  * ``` git rm -r --cached . ``` Clear cached file..Start again
  * ``` git remote ``` To see origin
  * ``` git remote add origin repisitory_link ``` Repisitory_link from github
### Git Conflict resolve: ###
  * ``` git --rebase origin master ``` 
  * ``` git mergetool ``` It will open interface, you need to resolve conflict by your own
  * ``` git rebase continue ```
  * ``` git push ```
### Git Stash (Temporary Storage) ###
  * ``` git stash ``` Create temporary location to save changes file. It will also use for revert changes
  * ``` git stash apply ``` You can apply stash file changes on current branch. Last stash file will not be removed from stash
  * ``` git stash pop ```  It will remove last stash file from stash
  * ``` git stash drop ``` Clean stash file 
### Git commit history & delete (Temporary Storage) ###
  * ``` git log ``` (To check  commit)
  * ``` git reset --soft HEAD~1 ``` Delete last commit
  * ``` git reset --soft HEAD~2 ``` Delete last two commit
### Git for parent branch ###
  * ```git show-branch | grep '*' | grep -v "$(git rev-parse --abbrev-ref HEAD)" | head -n1 | sed 's/.*\[\(.*\)\].*/\1/' | sed 's/[\^~].*//' ``` Show nearest parent branch
