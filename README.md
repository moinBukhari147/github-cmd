# Github Commands


## GitHub Branches Structure:

- Main: Contain the tested stable production ready code.
- Development: Integration branch where all feature branches are merged after review. Contains work-in-progress but mostly functional code.
- yourname/feature-name: Personal feature branches. On which the one working.

## GitHub Work flow

1. Start New Work

```bash
    git clone https://github.com/moinBukhari147/reshta-frontend.git
    git checkout develop
    git pull origin develop
    git checkout -b yourname/feature-name
```

2. Push and Work

````bash
    git push -u origin yourname/feature-name
    ```
````

3. Open a Pull Request

- Once your feature is ready, open a PR from your branch into develop on GitHub.
- Tag a reviewer and fix any issues before merging.

4. Merge to Develop

- After approval and testing, your branch is merged into develop.

5. Release to Main

6. After Merge Cleanup

```bash
    git branch -d yourname/feature-name
    git push origin --delete yourname/feature-name

```

## 💡 Tips

Always branch from develop, not from your last feature.

Pull latest changes before starting new work.

Keep PRs small and focused to reduce review time and conflicts.

Use meaningful branch names, like yourname/login-screen or collab/otp-bugfix.

## Ohter Commands

- #### View Log history

```bash
   git reflog
```
Git reflog is your private, local undo/redo history, tracking every change you make—even those not visible to others.
Use git reflog to recover from mistakes or see all local changes, even those not in the current branch history.


- View Log history 2nd Methods

```bash
   git log
```
Git log is the public, polished history of your project.
Use git log to see the official commit history; 

- Hard reset

```bash
   git reset --hard 82497d1
```
To reset branch back to that state: your [state_id]

- To view your commit history in a simple and compact format.

```bash
   git log --oneline
```
- View Visual Commit History Across All Branches
  
```bash
   git log --oneline --graph --all --decorate
```
Shows a compact, visual representation of the entire Git commit history, including all branches, with references like tags and HEAD clearly labeled.

### Diff

- Check unstaged changes
```bash
   git diff
```
Shows changes in your working directory not yet staged for commit.

- Check staged changes (before committing)
```bash
   git diff --staged
```
Shows changes that have been staged using git add but not committed yet.

- Compare your local branch with the last commit
```bash
   git diff HEAD
```
Shows all changes (both staged and unstaged) compared to the latest commit.

- Compare two branches
```bash
   git diff branchA..branchB
```
Shows changes in branchB that are not in branchA.

- Compare two commits
```bash
   git diff commit1 commit2
```
Shows differences between two specific commits.

- Compare specific files
```bash
   git diff HEAD path/to/file.js
```
Shows changes in a specific file compared to the last commit.

### Stash

- Stash your changes
```bash
   git stash
```
Git stash temporarily shelves (or "stashes") uncommitted changes in your working directory so you can, Switch branches, Pull/rebase, Work on something else Without committing or losing your work.

- List all stashes
```bash
  git stash list
```

- Apply the latest stash
```bash
  git stash apply
```
Keeps the stash in stash list (does not remove it)

-  Apply and remove the stash
```bash
  git stash pop
```
Applies and removes the latest stash
-  Apply a specific stash
```bash
  git stash apply stash@{1}
```
-  Drop (delete) a stash
```bash
  git stash drop stash@{0}
```
-  Clear all stashes
```bash
  git stash clear
```

  


  
  
  



