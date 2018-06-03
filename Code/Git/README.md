# Git in Practice

### CHAPTER 1. Local Git

###### 1-Setup

git config --global user.email   
git init GitInPracticeRedux  
git add  
git commit --message 'Initial commit of book.  

###### 2-Object Store

###### 3-Others
SHA - 160-bit (20-byte) hash value  
git log  
gitx, gitk  

###### 4-Rewriting history
Squash commits that are related  
EG: 1-Add window 2- fix 3-fix 4-Add button
Squash: 1-Add window 4-Add button


git diff

###### 5-Refs
git diff master~1 master  
git rev-parse master

### CHAPTER 2. Remote Git

###### 6-Adding a remote repository: git remote add
git remote add origin https://github.com/arunsivakumar/GitInPracticeRedux.git  

git remote --verbose  

###### 7-Pushing changes to a remote repository: git push
git push --set-upstream origin master (First time)  
git push

###### 8-Cloning a remote/GitHub repository onto your local ma- achine: git clone
git clone https://github.com/GitInPractice/GitInPracticeRedux.git<br/>

--recursive -submodules

###### 9-Pulling changes from another repository: git pull
git pull

###### 10-Technique 10 Fetching changes from a remote without modifying
git fetch

###### 11-Creating a new local branch from the current branch: git branch
git branch chapter-two

###### 12-Checking out a local branch: git checkout
git checkout chapter-two
git checkout --force (ignore changes in master)
git stash (stach master)

###### 13-Pushing a local branch remotely
git push --set-upstream origin chapter-two

###### 14-Merging a branch
git merge  

###### 15-Deleting a remote branch
git push --delete origin chapter-two  

###### 16-Deleting the current local branch after merging
git branch --delete chapter-two  

### PART-2
### CHAPTER 3. FileSystem interactions

###### 17-Renaming or moving a git file: git mv
###### 18-Removing a file: git rm
###### 19-Resetting files to last commit : git reset
--hard to reset staging and working  
--mixed default  
* use stash instead

###### 20- Deleting untracked files: git clean
other tracked files - git ls-files -o  
 git clean --force  
 git clean -n (safer)
 git clean --force -x
###### 21-Ignoring files: .gitignore
###### 22-Deleting ignored files
###### 23-Stashing changes: git stash
git diff stash@{0}  

###### 24-Reapply stashed changes: git stash pop
###### 25-Clearing stash: git stash clear

###### 26-Assuming files are unchanged??
###### 27-Listing assumed-unchanged files??
###### 28-Stopping assuming files are changed??

### CHAPTER 4. History Visualization

###### 29-Listing certain commits
git log --author "Mike McQuaid" --after "Nov 10 2013" --grep 'file\.'  
glo --author "Arun Sivakumar" --after "June 1 2018"  
git show - shows a single commit

###### 30-Listing commits with different formatting??
###### 31-Releasing shortlogs: gitshortlog??

###### 32-Finding bug: git bisect

### CHAPTER 5. Advanced Branching

###### 33-Merging branches and always creating merge commit
git merge --no-ff chapter-spacing
merge commit - 2 parents
1. previous commit on the current branch(master)
2. previous commit on the incoming branch

######Strategy
1. recursive
2. octopus
3. ours
4. subtree

###### 34-Resolving merge conflict
git mergetool -t opendiff

###### 35-Resolving each merge conflict only once - git rerere??

###### 36-Creating a tag - git tag
* --list list --v0.*
* --force update to new pint
* --delete

###### 37-Generating version number based on tags
git describe --tags

###### 38-Adding a single commit to the current branch: git cherry-pick
###### 39-Reverting a previous commit: git revert
###### 40- Listing what branches contain a commit: git cherry
git cherry --verbose master
shows the diff from master

### CHAPTER 6.Rewriting history and disaster recovery

###### 41-Listing all changes including history rewrites: git reflog
###### 42-Resetting a branch to a previous commit: git reset
###### 43- Rebasing commits on top of another branch: git rebase
###### 44- Rebasing commits interactively: git rebase --interactive
###### 45- Pulling a branch and rebasing commits: git pull --rebase
###### 46- Rewriting history on a remote branch: git push --force
###### 47- Rewriting the entire history of a branch: git filter-branch

###Part 3. Advanced Git
###Chapter 7. Personalizing Git

###### 48- Setting the configuration for all repositories
###### 49- Setting the configuration for a single repository
###### 50-Aliasing commands
###### 51- Showing the current branch in your terminal prompt

###Chapter 8. Vendoring dependencies as submodules

###### 52- Adding a git submodule: git submodule add
###### 53- Showing the status of submodules: git submodule status
###### 54- Updating and initializing all submodules: git submod- dule update --init
###### 55- Running a command in every submodule: git submodule foreach

###Chapter 9. Working with Subversion

###### 56-Refs
###### 57-Refs
###### 58-Refs

###Chapter 10. GitHub pull requests

###### 59- Making a pull request in the same repository: gh pull-request
###### 60- Making a pull request from a forked repository: gh fork
###### 61- Merging a pull request from the same repository
###### 62- Merging a pull request from a forked repository: gh merge

###Chapter 11. Hosting a repository
###### 63-  Initializing a local repository in a server hosting - format: git init --bare
###### 64- Mirroring a repository: git clone --mirror
###### 65- Sharing a repository with other users on the same ne- etwork: git daemon

###Part 4. Git best practices

###Chapter 12. Creating a clean history

###Chapter 13. Merging vs. rebasing

###Chapter 14. Recommended team workflows
