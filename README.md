# learn Git & Github on fireship.io

## git started

### git init

A commit = a snapshot. The repository keeps these snapshots.

By deleting the .git folder, git will be completely gone.

### git status

Create a .gitignore file to ignore unwanted files.

### git add

`git add` is needed before commit.

`git add .` can add all files in the folder.

The opposite of `git add` is `git reset`.

### git commit

`git commit -m "some messages"`

Use `git log` to check commit information.

`git commit -a -m "some messages"` Add files and commit in a single command.

## remote

### git remote

List current remote info: `git remote -v`

Create a new remote: `git remote add origin <url-to-your-repo>` 

### git push

`git push origin master -u`

`origin` is the name of the remote; `master` is the name of the branch.
`-u` is optional to set origin to upstream remote (needed when using pull)

### git fetch/merge

When some updates are made on github (orgin/master), there're two ways to sync the update to local. Fetch and merge is one of them.

`git fetch` and then `git merge origin/master`

### git pull

pull = fetch + merge

`git pull origin master` Since we used `-u` in push command,  `git pull` is enough.

### git clone

`git clone <url-to-repo> <folder-name>`

Can cd into the folder and use `git pull` to get the newest code from the repo.

## collaboration

### git branch

`git branch` list all local branches.

`git branch -M <new-name>` change the name of the current branch.

`git branch <new-branch-name>` create a new branch.

`git branch -d <branch-name>` delete a branch. `-d` delete if merged. `-D` force delete.

### git checkout

`git checkout -` go to the last branch.

### Merge Conflict

When merge conflict happens, `git diff` to see the difference. `git merge --abort` to go back to before merge.

With vscode UI, just choose the right option and make a new add+commit.
