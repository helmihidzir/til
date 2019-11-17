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

