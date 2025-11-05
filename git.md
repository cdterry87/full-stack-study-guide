# Git Study Guide

## 🧩 Beginner Level

- **Q:** What is Git?  
  **A:** A distributed version control system to track code changes and collaborate efficiently.

- **Q:** What is the difference between Git and GitHub?  
  **A:** Git is a version control tool; GitHub is a cloud platform for hosting Git repositories.

- **Q:** What is a repository (repo)?  
  **A:** A storage space for your project’s files and Git history.

- **Q:** What is the difference between a local and remote repository?  
  **A:** Local: on your machine; Remote: hosted server (GitHub, GitLab, etc.).

- **Q:** What is a commit?  
  **A:** A snapshot of your code with a message describing the changes.

- **Q:** What is the staging area?  
  **A:** A temporary space to prepare files for a commit (`git add`).

- **Q:** How do you initialize a Git repository?  
  **A:** `git init`

- **Q:** How do you clone a repository?  
  **A:** `git clone <repo-url>`

- **Q:** How do you check the status of files?  
  **A:** `git status`

- **Q:** How do you add changes to a commit?  
  **A:** `git add <file>` or `git add .` for all files

- **Q:** How do you create a commit?  
  **A:** `git commit -m "message"`

- **Q:** How do you view commit history?  
  **A:** `git log` (add `--oneline` for short view)

- **Q:** How do you discard local changes?  
  **A:** `git checkout -- <file>` or `git restore <file>`

---

## ⚙️ Intermediate Level

- **Q:** What is the difference between `git pull` and `git fetch`?  
  **A:**

  - `fetch`: downloads changes but does not merge
  - `pull`: fetch + merge automatically

- **Q:** What is a branch in Git?  
  **A:** A parallel line of development to work on features or fixes independently.

- **Q:** How do you create a new branch?  
  **A:** `git branch <branch-name>` or `git checkout -b <branch-name>`

- **Q:** How do you switch branches?  
  **A:** `git checkout <branch-name>` or `git switch <branch-name>`

- **Q:** How do you merge branches?  
  **A:** `git merge <branch-name>` into the current branch

- **Q:** What is a fast-forward merge?  
  **A:** A merge where the branch pointer moves forward without creating a merge commit.

- **Q:** What is a merge conflict and how do you resolve it?  
  **A:** Conflicting changes in the same file; resolve manually and commit.

- **Q:** What is `git stash`?  
  **A:** Temporarily save changes to reapply later (`git stash`, `git stash pop`).

- **Q:** How do you undo a commit that hasn’t been pushed?  
  **A:** `git reset --soft HEAD~1` (keeps changes staged)  
  `git reset --hard HEAD~1` (discards changes)

- **Q:** How do you view differences between commits?  
  **A:** `git diff` or `git diff <commit1> <commit2>`

- **Q:** How do you push changes to a remote branch?  
  **A:** `git push origin <branch-name>`

- **Q:** How do you pull changes from a remote branch?  
  **A:** `git pull origin <branch-name>`

- **Q:** How do you delete a branch?  
  **A:** Local: `git branch -d <branch>`  
  Remote: `git push origin --delete <branch>`

- **Q:** What is a tag in Git?  
  **A:** A marker for specific commits (e.g., releases): `git tag v1.0.0`

---

## 🧠 Advanced Level

- **Q:** What is rebasing and why use it?  
  **A:** Rewriting commit history to apply changes on top of another branch (`git rebase <branch>`). Keeps history linear.

- **Q:** What is the difference between merge and rebase?  
  **A:** Merge preserves commit history; rebase rewrites history for linearity.

- **Q:** How do you squash commits?  
  **A:** `git rebase -i HEAD~n` and mark commits as `squash` to combine them.

- **Q:** What is cherry-picking?  
  **A:** Apply a specific commit from one branch onto another: `git cherry-pick <commit-hash>`

- **Q:** What is a detached HEAD?  
  **A:** Checking out a commit instead of a branch, so HEAD is not attached to any branch.

- **Q:** How do you resolve a detached HEAD situation?  
  **A:** Create a branch from the current commit: `git checkout -b <branch-name>`

- **Q:** How do you find commits by author or message?  
  **A:** `git log --author="name"` or `git log --grep="message"`

- **Q:** How do you revert a pushed commit?  
  **A:** `git revert <commit>` (creates a new commit that undoes changes)

- **Q:** What is reflog and why is it useful?  
  **A:** Tracks all HEAD movements; allows recovering lost commits: `git reflog`

- **Q:** How do you manage multiple remotes?  
  **A:** `git remote add <name> <url>`; push/pull using `git push <name> <branch>`

- **Q:** How do you handle large binary files in Git?  
  **A:** Use Git LFS (Large File Storage) to track them efficiently.

- **Q:** How do you squash and merge in GitHub?  
  **A:** On PR, select "Squash and merge" to combine commits into one before merging.

- **Q:** What are Git hooks?  
  **A:** Scripts that run automatically on Git events (`pre-commit`, `post-merge`, etc.)

- **Q:** What is the difference between shallow and full clones?  
  **A:** Shallow: only latest commits (`--depth 1`); Full: entire history.

- **Q:** How do you protect a branch?  
  **A:** Enable branch protection rules in GitHub/GitLab: require PR reviews, status checks, and prevent force pushes.

- **Q:** How do you handle rebasing conflicts?  
  **A:** Resolve manually, then `git rebase --continue` or abort with `git rebase --abort`.

- **Q:** How can Git be used in CI/CD?  
  **A:** Trigger pipelines on push, pull request, or tag; automate builds, tests, and deployments.

- **Q:** How do you revert multiple commits safely?  
  **A:** Use `git revert <commit1>..<commitN>` to create new commits that undo the range.
