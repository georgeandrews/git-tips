# git-tips
Tips for using git that I often need to Google.

## GIT
### git pull --rebase
Pull, then apply any local commits on top.

### git branch --sort=-committerdate
Sort branches based on latest commit.

### git rebase -i <commit>
Interactive rebase allowing multiple commits to be reworded, dropped, squashed, fixed up, etc...

### git fetch <remote>; git checkout -b <branch> <remote>/<branch>;
Checks out remote branch locally.

### git config --global alias.serve "daemon --verbose --export-all --base-path=.git --reuseaddr --strict-paths --enable=receive-pack .git/"; git serve;
Colleagues can clone, pull, and push from peer to peer in LAN (e.g. when Github is down).

### git fetch -p
Fetch branches from remote while purging any deleted branches.

### git reset --soft HEAD~1
Delete commit, but keep changes. 

### git add -p
Add certain changes and not others. Or just to review additions.

### git reset --hard; git clean -df;
When testing something and you decide nah...

### git commit --allow-empty
Weird scenarios where you want a commit and message but no diffs (e.g. automation).

### git commit --amend --no-edit
Commit changes to previous commit without having to create and squash a new commit.

### git bisect
Useful for hunting down bugs.

### git branch --merged | egrep -v "(^\*|master|develop)" | xargs git branch -d
Delete all local branches already merged into currently checked out branch (except master and develop).

### git reflog
List of all hashes of every change made in git.

### git reset --mix master; git add -p;
Revert branch to master mixed with your commit history; then allows using history to add only selected commits.

### git commit --amend --CHEAD
All unstaged changes are added to most recent commit, keeping previous commit message.

### git fetch && git rebase --autostash --keep-merges
Get up to date with tracking branch without needing a clean workspace.

### git cherry-pick -x <commit>
Cherry pick a commit while keeping original commit message.

### git diff --staged
Shows diff from files yet to be committed.
