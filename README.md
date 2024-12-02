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

`git log --graph --oneline --decorate` to see a more beautiful log.

## remote

### git remote

List current remote info: `git remote -v`

Create a new remote: `git remote add origin <url-to-your-repo>` 

### git push

`git push origin master -u`

`origin` is the name of the remote; `master` is the name of the branch.
`-u` is optional to set origin to upstream remote (needed when using pull)

`--force` to overwrite the remote commit. Will lost commits that is not in local.

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

## Advanced

### git reset

`git reset` by it self to unstage files in the staging area.

`git reset <commit ID>` to go back go the designated commit while keeping the changes unstaged for further edit.

`git reset --hard <commit ID>` to go back and completely discard changes.

Do not reset when a commit is pushed to Github.

Commonly use `git fetch` and `git reset --hard origin/master` to override local code with the remote code when something frustrating happened locally.

### git revert

`git revert <commit-ID-of-the-bad-commit>` to move back to previous commit. 

Unlike git reset, git revert keeps the bad commit and creates a new commit for going back to the previous commit. So the revert can be successfully pushed to remote.

### git commit --amend

`git commit --amend -m "new message"` to update the message of last commit.

`git commit --amend --no-edit` to commit the staged file that was fogoten to stage in last commit.

### git stash

Store changes for later use that is not worthy of a new branch or commit.

`git stash` to remove the modification. `git stash pop` to apply the changes back to the code.

`git stash save <name-of-stash>` to give the changes a name. `git stash list` to see all stashes and their index. `git stash apply <index>` to apply a certain stash.

### git rebase

A simpler way to keep feature branch in sync with main branch without merge commit.

`git rebase master` change the history of the current branch, as if the commits of the branch is based on the updated master.

### squash 

`git rebase master --interactive` to squash some commits into one to simplify the commit history.

