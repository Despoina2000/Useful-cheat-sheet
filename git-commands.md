- Setup & Configuration
```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global color.ui auto
git config --list
```

- Initialize & Clone
```
git init — Initialize a repository
git init <dir>
git clone <url>
git clone --branch <branch> <url>
```

- Basic Workflow
  - Check Status & Differences
    ```
    git status
    git diff
    git diff --staged
    ```

  - Stage Files
    ```
      git add <file>
      git add .
      git add -p
      ```

  - Commit Changes
      ```
    git commit -m "message"
    git commit -am "message"
    git commit --amend
    ```

- Branching & Switching
```
git branch
git branch <name>
git branch -d <name>
git switch <name>
git checkout <name>
git checkout -b <name>
```

- Merging & Rebasing
```
git merge <branch>
git rebase <branch>
git merge --squash <branch>
git cherry-pick <commit>
```

- Remote Repositories
```
git remote -v
git remote add origin <url>
git fetch
git pull
git pull --rebase
git push
git push -u origin <branch>
```

- Undoing Changes
```
git restore <file>
git restore --staged <file>
git reset <commit>
git reset --hard <commit>
git clean -f
git revert <commit>
```

- History & Inspection
```
git log
git log --oneline
git log --graph
git show <commit>
git blame <file>
git reflog
```

- Stashing
```
git stash
git stash list
git stash pop
git stash drop
```

- File Operations
```
git rm <file>
git mv <old> <new>
```

- Tags
```
git tag
git tag <name>
git tag -a <name> -m "message"
```
