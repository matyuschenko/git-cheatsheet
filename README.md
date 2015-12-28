# git-cheatsheet
:octocat: Useful GIT commands

#####MAIN
git status<br />
git add 2015/dec31/dec31/main.js<br />
git commit -m "Bug fixed"<br />
git push -u origin december-31-mmaks-local<br />
(make pull request on web)<br />
(after pull request accepted)<br />
git pull (== git fetch; gir merge origin/master)<br />

#####BASIC
git init<br />
git status<br />
git log; git log --pretty=oneline<br />
git hist (my alias for git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short)

#####SAVE & COMMIT
git add file1.txt<br />
git diff file1.txt<br />
git commit -m ‘message’

#####REMOTE
git clone http...<br />
git fetch (update local with remote, but not merge)<br />
git merge origin/master<br />
git rebase origin/master<br />
git pull (== git fetch + git merge)<br />
git pull --rebase (== git fetch + git rebase)<br />
git push (apply local changes to remote)<br />

git remote<br />
git remote show origin<br />
git branch --track style origin/style (add local branch to track remote branch)

#####BRANCHES
git checkout -b name (make branch and switch to it; == git branch name + git checkout name)

#####UNDO
git reset HEAD~1<br />
git reset --hard v1 (reset to tag v1)<br />
git revert HEAD (cancel last commit)<br />
git checkout hello.html (cancel unstaged changes)<br />
git reset HEAD hello.html (cancel staged changes; does not change actual file)<br />
git commit --amend -m ‘amended commit’ (amend last commit)

#####MOVE
git checkout afd45c2<br />
git checkout HEAD^^ (two up from HEAD)<br />
git checkout master~4 (four up from master)

#####ALIAS
git config --global alias.ci commit<br />
git config --global alias.st status<br />
git config --global alias.br branch<br />
git config --global alias.hist 'log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short'<br />
git config --global alias.type 'cat-file -t'<br />
git config --global alias.dump 'cat-file -p'
