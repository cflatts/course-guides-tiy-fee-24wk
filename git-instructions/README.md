Start a project (do once for each project)
==========================================

1. Initialize a local repository: `git init`
2. Initialize a remote repository: `hub create`

If you do not have `hub` (test by running `which hub` anywhere in the terminal)
-----------------------------------------------------------------------------------------------------

2. Create a new repository on github.com
3. Where you have initialized the local repository run `git remote add origin git@github.com:[GITHUB USERNAME]/[NAME OF REMOTE REPOSITORY].git`

Commands to run while working on a project
==========================================

* Stage a new commit: `git add [CHANGES YOU WANT STAGED]`
* Commit changes: `git commit -m "[DESCRIPTION OF CHANGES]"`
* Push commits to remote repo: `git push origin [NAME OF BRANCH]`

* Check what branch you're on: `git branch`
* Check what changes need to be commited AND what branch you're on: `git status`
* Create AND switch to new branch: `git checkout -b [NAME OF NEW BRANCH]`
* Switch to a branch: `git checkout [NAME OF BRANCH]`
* Merge branches: MAKE SURE YOU ARE IN THE BRANCH YOU WANT TO PULL THE CHANGES TO `git merge [BRANCH YOU ARE PULLING CHANGES FROM]`
