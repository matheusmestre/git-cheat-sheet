## Contents

* [Setup Commands](#setup-commands)
* [General Commands](#general-commands)
  * [git --version](#git---version)
  * [git config](#git-config)

# general commands

#### git --version
Check installed Git version
```
git --version
```
#### git config
Configure user information globally. Omit `--global` parameter to set the information just to the current repository
```
git config --global user.name "<userName>"
git config --global user.email "<email>"
```
#### git init
Create empty Git repository
```
git init
```
#### git status
Check working directory and staging area status
```
git status
```
#### git log
Display all commits of current branch
```
git log
```
#### git ls-files
List all data/files in the staging area
```
git ls-files
```

# commits

#### Add file(s) to the staging area
Add single file or all working directory files to the staging area
```
git add <fileName>
git add .
```
#### Removing files
Run command after file was deleted from working directory. This will add the file deletion to the staging area
```
git rm <filename>
git add <filename>
```
#### Create new commit
```
git commit -m "<message>"
```
#### Checkout commit
```
git checkout <commit-id>
```

# branches

#### List branches
````
git branch
````
#### Create branch
````
git branch <branch name>
````
#### Go to branch
````
git checkout <branch name>
git switch <branch name>
````
#### Create and switch to new branch
````
git checkout -b <branch name>
git switch -c <branch name>
````
#### Delete branch
````
git branch -d <branch name>
git branch -D <branch name>
````

# stash
Temporarily store modified, tracked files in order to change branches

##### Show stash list
```
git stash list
```
##### Create stash entry
```
git stash
git stash push -m "<message>"
```    
##### Apply stash entry to WD
```
git stash apply
git stash apply <stash-index>
```
##### Remove stash entry
```
git stash drop <stash-index>
```
##### Remove stash and apply to WD
```
git stash pop <stash-index>
```
##### Clear stash list
```
git stash clear
```

# reflog

##### Show Reflog List
A log of all project changed made including deleted commits.
```
git reflog
```
##### Reset the WD to the reflog state
```
git reset --hard <reflog-id>
```
##### Checkout the reflog state to detached head
```
git checkout <reflog-id>
```

# tagging

##### Show tag list
```
git tag
```
##### Tag a commit
```
git tag <tag-name> <commit-id>
git tag -a <tag-name> -m <message> <commit-id>
```
##### Show tag info
```
git show <tag-name>
```
##### Checkout to the tagged commit
```
git checkout <tag name>
```
##### Remove tag
```
git tag -d <tag-name>
```
