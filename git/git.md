# Git

Delete branch
```bash
git branch -d/D <branch name>
```

Find remote repository
```bash
git remote -v
```

Push for the first time
```bash
git push -u origin master
```

Force push
```bash
git push --force
```

Add remote origin
```bash
git remote add origin <link>.git
```

Pull update from remote master (useful in open source contribution)
```bash
git pull upstream master
```

Reset to specific commit
```bash
git reset --hard <commit id>
```

Enable `git lg` which has a better presentation than `git log`
```bash
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```

To get rid of this message after `git rebase`,

```
On branch dev
Your branch is up-to-date with 'dropbox/dev'.
You are currently editing a commit while rebasing branch 'Releases' on '72ca998'.
  (use "git commit --amend" to amend the current commit)
  (use "git rebase --continue" once you are satisfied with your changes)

nothing to commit, working directory clean
```

run, `git rebase --abort`. [Source](https://stackoverflow.com/questions/31252363/how-to-get-rid-of-message-strange-message-on-git-status)

Remove certain file from git 
```bash
git rm --cached <filename>
```