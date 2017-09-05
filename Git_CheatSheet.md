# **Some Git Commands & Examples** 
#### (basic commands,not an exhaustive list):
------------------------------------------------------------------------------------------------------------------------------------------

**Git Command** | **Task Description** | **Notes** 
:-----|:-----|:-----
`git init`| initializes an empty Git (local) repo in the directory it is called from|  also creates hidden .git folder
`git status`| shows status of repo| run this often especially before committing changes!!
`git add <filename>`| adds file to the staging area
`git add -A .`| same as above, but the dot stands for the current dir., so everything in & under it is added| -A ensures even file deletions are included.
`git add '*.txt'`| using wildcards to add files in the current folder and all sub-folders under it|Wildcards: We need quotes so that Git will receive the wildcard before our shell can interfere with it. Without quotes our shell will only execute the wildcard search within the current directory. Git will receive the list of files the shell found instead of the wildcard and it will not be able to add the files inside of any sub-directory if they exist.
`git reset <filename>`| to remove a file(s) from the staging area.
`git commit -m “some description here”`| This stores our stages changes to the repo.|commit command with a message describing what we've changed.
`git log`| see all commits (changes) made to the repo in the order/when they were made.
`git log --summary`|to see more information for each commit| You can see where new files were added for the first time or where files were deleted. It's a good overview of what's going on in the project. 
`git remote`|add a remote repository|This command creates a remote repo and needs a remote repo name and a repository URL (where an empty repo has been initialized) Ex: `git remote add origin https://github.com/try-git/try_git.git` 
`git push`|pushes commits to remote repo|Ex: `git push -u origin master` (The name of our remote is origin in above example and the default local branch name is master.
`git pull`|check for changes on our GitHub remote repo and pull down any new changes to say, a local repo.|Ex. : `git pull origin master`
`git checkout <target>`| to (re)set the state of repo to target which is shown next to commit when you do a git log|Ex: `git checkout 7499a39992a606fb86caa86f161ff7f33483648234287`.  You can view the previous state of your files here. To return to the master branch to see the most current state of your files, do: `git checkout master`
`git branch <branch name>`|creates a copy (or branch) of the main code
`git branch`| list all branches
`git checkout <branch name>`| switch to branch name
`git rm <filenames>`| to delete files and stage for commit, all in one step.
`git checkout master`|switch to master branch
`git merge <branch-name>`| to merge changes comitted to branchname back into the master
`git branch -d <branch-name>`|to delete a branch| Works for branches that have already been merged with master. For un-merged or abandoned branches, use the -f flag too.



# **Some Important Definitions**
------------------------------------------------------------------------------------------------------------------------------------------

**Term**| **Description**
:---|:---
Staging Area| A place where we can group files together before we "commit" them to Git.
Commit| A commit is a snapshot of our repository. This way if we ever need to look back at the changes we've made (or if someone else does), we will see a nice timeline of all changes.
Staged| files that are ready to be committed (say after `git add`)
Unstaged| Files with changes that have not been prepared to be committed (that are currently being tracked by git).
Untracked| Files aren't tracked by Git yet. This usually indicates a newly created file or files were haven't stages yet because perhaps we don't want them tracked'.
Deleted|File has been deleted and is waiting to be removed from Git.
HEAD| The HEAD is a pointer that holds your position within all your different commits. By default HEAD points to your most recent commit, so it can be used as a quick way to reference that commit.
Branching| When developers are working on a feature or bug they'll often create a copy (aka. branch) of their code they can make separate commits to. Then when they're done they can merge this branch back into their main master branch. Branches are what naturally happens when you want to work on multiple features at the same time. You wouldn't want to end up with a master branch which has Feature A half done and Feature B half done. Rather you'd separate the code base into two "snapshots" (branches) and work on and commit to them separately. As soon as one was ready, you might merge this branch back into the master branch and push it to the remote server.
Pull Requests| If you're hosting your repo on GitHub, you can do something called a pull request. A pull request allows the boss of the project to look through your changes and make comments before deciding to merge in the change. It's a really great feature that is used all the time for remote workers and open-source projects.


Standard Disclaimer: All info. above has been gleaned from this [awesome Git tutorial](https://try.github.io/levels/1/challenges/1)



