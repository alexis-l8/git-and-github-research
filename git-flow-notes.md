# Git notes

Alexis is working on his startup, alone. He:
+ Creates a repo with `README.md`
+ Clones the repo to his machine [`git clone <url>`]
+ Creates a branch to work on a new feature [`git checkout -b <new-branch-name>`]
+ Writes some new code
+ Adds and commits this code [`git add <changed-filename>` and `git commit -m '<Commit message>'`]
+ Pushes the new branch to Github [`git push origin <new-branch-name>`]
+ Visits repository on github.com

**Good Practice**
+ Switches branch to `<new-branch-name>`
+ Creates new pull request detailing changes

**Bad Practice***
+ Merges pull request with `master`
+ Deletes the branch

**Good Practice**
+ Pulls changes to his machine with `git pull`
+ Deletes the branch locally with `git branch -d <new-branch-name>`

Oli joins Alexis' startup
+ Alexis adds Oli as a collaborator
+ This means he can directly push files to the repo
+ Oli clones Alexis' repo directly (rather than forking)
+ Oli makes a change to Alexis' code

**Bad Practice**
+ Like an idiot Oli edits `master` and pushes

Meanwhile:
+ Alexis creates a new feature branch
+ He pushes this branch and creates a new pull request
+ There is a merge conflict as Oli had edited `master`
+ Alexis resolves the conflict in the web editor
+ He assigns Oli the pull request
+ Oli checks the request and merges it, deleting the branch
+ They both `git pull` and promise not to push to `master` ever again
