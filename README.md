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