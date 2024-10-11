Here’s a list of essential Git commands that you’ll frequently use in version control:

### 1. **Setup and Configuration**
- `git config --global user.name "Your Name"`  
  Set the name you want to use for all commits.

- `git config --global user.email "you@example.com"`  
  Set the email you want to use for all commits.

- `git config --list`  
  View all Git configurations.

### 2. **Repository Commands**
- `git init`  
  Initialize a new Git repository.

- `git clone <repository-url>`  
  Clone an existing repository to your local machine.

### 3. **Basic Workflow**
- `git status`  
  Check the current status of your repository (staged, modified, untracked files).

- `git add <file>`  
  Stage a file for the next commit.

- `git add .`  
  Stage all changed files in the current directory for the next commit.

- `git commit -m "Commit message"`  
  Commit the staged changes with a message.

- `git commit -am "Commit message"`  
  Stage and commit all tracked files in one step (not for new files).

### 4. **Branching**
- `git branch`  
  List all branches in your repository.

- `git branch <branch-name>`  
  Create a new branch.

- `git checkout <branch-name>`  
  Switch to an existing branch.

- `git checkout -b <branch-name>`  
  Create and switch to a new branch.

- `git merge <branch-name>`  
  Merge the specified branch into the current branch.

- `git branch -d <branch-name>`  
  Delete a branch.

### 5. **Pushing and Pulling**
- `git push`  
  Push committed changes to the remote repository.

- `git push origin <branch-name>`  
  Push a specific branch to the remote repository.

- `git pull`  
  Fetch and merge changes from the remote repository.

### 6. **Remote Repositories**
- `git remote add origin <remote-url>`  
  Add a remote repository.

- `git remote -v`  
  View the remote repositories linked to your local repository.

- `git push origin --delete <branch-name>`  
  Delete a branch from the remote repository.

### 7. **Undoing Changes**
- `git reset <file>`  
  Unstage a file that has been added.

- `git reset --hard <commit>`  
  Reset the working directory and index to a specific commit, discarding changes.

- `git revert <commit>`  
  Revert a commit by creating a new commit that undoes the changes.

### 8. **Logs and History**
- `git log`  
  View the commit history.

- `git log --oneline`  
  View the commit history in a compact format.

- `git diff`  
  Show the differences between the working directory and the last commit.

- `git show <commit>`  
  Display the changes in a specific commit.

### 9. **Stashing**
- `git stash`  
  Temporarily save changes that are not ready to be committed.

- `git stash pop`  
  Reapply the changes from the stash.

### 10. **Tags**
- `git tag <tag-name>`  
  Create a new tag.

- `git tag`  
  List all tags.

### 11. **Collaborative Commands**
- `git fetch`  
  Download changes from the remote repository without merging.

- `git rebase <branch-name>`  
  Reapply commits on top of another base branch.

### 12. **Working with Commit History**
- `git cherry-pick <commit>`  
  Apply the changes from a specific commit to the current branch.

- `git reflog`  
  Show a log of all reference updates, including branch changes and resets.

- `git log --graph --decorate --oneline --all`  
  Visualize the repository history in a graph-like structure, showing branches and merges.

- `git blame <file>`  
  Show the author and commit information for each line of a file.

### 13. **Interactive Staging and Rebasing**
- `git add -p`  
  Interactively stage changes, allowing you to pick which changes to add.

- `git rebase -i <commit>`  
  Interactive rebase, allowing you to squash, edit, or reorder commits.

### 14. **Squashing Commits**
- `git rebase -i HEAD~n`  
  Rebase the last `n` commits interactively to squash them into fewer commits.

- `git commit --amend`  
  Amend the last commit with new changes or update the commit message.

### 15. **Tagging (Extended)**
- `git tag -a <tag-name> -m "Tag message"`  
  Create an annotated tag with a message.

- `git push origin <tag-name>`  
  Push a tag to the remote repository.

- `git push --tags`  
  Push all tags to the remote repository.

### 16. **Advanced Branching and Merging**
- `git merge --no-ff <branch-name>`  
  Merge a branch, creating a merge commit even if the merge could be fast-forwarded.

- `git merge --squash <branch-name>`  
  Squash all changes from a branch into a single commit before merging.

- `git cherry <branch-A> <branch-B>`  
  Show commits in branch B that are not in branch A.

### 17. **Advanced Remote Management**
- `git remote show origin`  
  Show detailed information about the remote repository.

- `git remote prune origin`  
  Remove references to remote branches that have been deleted.

- `git fetch --all --prune`  
  Fetch all updates from the remote repository and remove outdated references.

### 18. **Submodules**
- `git submodule add <repository-url> <path>`  
  Add a submodule to your repository.

- `git submodule init`  
  Initialize submodule configuration.

- `git submodule update`  
  Fetch and update the submodules to the latest commit.

- `git submodule foreach <command>`  
  Run a command in each submodule.

### 19. **Git Bisect (Finding Bugs)**
- `git bisect start`  
  Start a binary search to find the commit that introduced a bug.

- `git bisect good <commit>`  
  Mark a commit as good (before the bug was introduced).

- `git bisect bad <commit>`  
  Mark a commit as bad (after the bug was introduced).

- `git bisect reset`  
  Reset after the bisect process is finished.

### 20. **Cleaning Up**
- `git clean -f`  
  Remove untracked files from the working directory.

- `git clean -fd`  
  Remove untracked files and directories.

- `git gc`  
  Cleanup unnecessary files and optimize the local repository.

### 21. **Git Hooks**
- Git hooks allow you to automate tasks. Some common hooks:
  - `pre-commit`: Run scripts before committing changes (e.g., code formatting, linting).
  - `post-merge`: Automatically run commands after a merge (e.g., run tests).
  - `pre-push`: Run scripts before pushing to the remote repository.

Hooks are stored in the `.git/hooks/` directory and can be customized.

### 22. **Git Worktrees**
- `git worktree add <path> <branch>`  
  Create a new working directory (worktree) with a specific branch.

- `git worktree list`  
  List all active worktrees.

### 23. **Handling Conflicts**
- `git mergetool`  
  Use a merge tool to resolve conflicts during a merge or rebase.

- `git diff --staged`  
  Show the differences between the staged files and the last commit.

- `git checkout --theirs <file>`  
  In case of a conflict, keep changes from the other branch.

- `git checkout --ours <file>`  
  In case of a conflict, keep changes from the current branch.

### 24. **Sparse Checkout (Partial Clone)**
- `git sparse-checkout init`  
  Initialize a sparse checkout (used for partial clones).

- `git sparse-checkout set <path>`  
  Set specific directories or files to be checked out in the working directory.

### 25. **Git Archives**
- `git archive --format=zip --output=archive.zip <branch-name>`  
  Create a zip archive of a specific branch.

---

These commands should give you a more comprehensive overview of Git's capabilities. Let me know if you’d like to dive deeper into any of these features!
