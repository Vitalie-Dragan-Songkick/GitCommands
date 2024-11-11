## Git Commands Cheat Sheet

| Command                                     | Description                                                                                           |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `git commit --amend -m "new commit"`        | Change last commit message.                                                                            |
| `git commit --amend --no-edit`              | Add files to the last commit without changing the commit message.                                      |
| `git push -f` / `git commit -f`             | Force a commit push or commit, even if you don’t have the latest changes.                              |
| `git log` / `git log --oneline`             | View commit logs (shorter version for `--oneline`).                                                   |
| `git revert <hashID>`                       | Revert a commit without removing it from commit history, restores previous state.                      |
| `git stash` / `git stash save <name>`       | Save current work in progress without committing it.                                                  |
| `git stash apply` / `git stash list`        | Apply stashed changes or view a list of stashes.                                                      |
| `git branch -M "new-production-branch"`     | Rename the current branch (typically used for production branches).                                    |
| `git checkout -`                            | Switch to the last used branch.                                                                        |
| `git clean -f`                              | Remove untracked files from the working directory (careful, cannot be undone).                        |
| `git clean -df`                             | Remove untracked files and directories (careful, cannot be undone).                                  |
| `git checkout master`                       | Checkout the master branch.                                                                            |
| `git pull`                                  | Pull the latest changes from the remote repository.                                                   |
| `git checkout your-branch-name`             | Checkout a specific branch.                                                                            |
| `git rebase master`                         | Rebase your branch onto the master branch (conflict resolution may be needed).                         |
| `git pull origin master`                    | Pull and rebase onto the master branch (may require conflict resolution).                              |
| `git reset --hard <hashID>` & `git push -f`  | **Never use if your branch was already pushed**. Resets the branch to a specific commit (can mess up others' work). |
| `git show-branch`                           | Display branches and their commit history.                                                            |
| `git diff <hash1> <hash2>`                  | Compare differences between two commits (view what is missing in hash1).                              |
| `git show <hashID>`                         | Show detailed information about a specific commit (who made the changes, etc.).                       |
| `git reflog`                                | View the history of your actions (commits, checkouts, rebases) in the repository.                     |
| `git reset --soft <hashID>`                 | Reset the branch to a specific commit but keep changes staged for future commits.                     |
| `git pull --no-commit`                      | Pull without automatically committing, allowing for inspection beforehand.                            |
| `git rebase --no-commit`                    | Rebase without automatically committing, allowing for inspection beforehand.                          |
| `git merge --no-commit`                     | Merge without automatically committing, allowing for inspection beforehand.                           |
| `git commit --fixup=hashID`                 | Create a fixup commit for a previous commit identified by `hashID`.                                    |
| `git rebase -i --autosquash HEAD~N`         | Squash a commit with some fixes into another commit as a fixup (N commits back).                      |
| `git bisect`                                | Helps identify the commit that introduced a bug by performing a binary search through commit history. |
| `git bisect start`                          | Start a bisect session to search for a bad commit.                                                     |
| `git bisect bad <LatestHash>`               | Mark a commit as "bad" during bisect.                                                                  |
| `git bisect good <WorkingHash>`             | Mark a commit as "good" during bisect.                                                                 |
| `git bisect reset`                          | End a bisect session and return to the normal state.                                                   |
