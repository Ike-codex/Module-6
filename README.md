# Advanced Git Basics: Clean, Cherry-Pick, Log, Merge Types, & Diffs

## 1. `git clean`
*   **What it does:** Removes untracked files (junk or generated files that haven't been added to Git yet) from your working directory.
*   **Common Commands:**
    *   `git clean -n` — "Dry run" that shows you what files *would* be deleted without actually deleting them.
    *   `git clean -fd` — Force deletes untracked files (`-f`) and untracked directories (`-d`).

## 2. Git Cherry-Picking (`git cherry-pick`)
*   **What it does:** Takes a single, specific commit from one branch and applies it onto your current active branch.
*   **Command:** `git cherry-pick <commit-hash>`
*   **Why use it:** Great for grabbing a bug fix or a specific feature from another branch without merging the whole branch.

## 3. `git log`
*   **What it does:** Displays the chronological commit history for your repository.
*   **Common Variations:**
    *   `git log` — Shows detailed history (author, date, full hash, and commit message).
    *   `git log --oneline` — Condenses each commit down to a single line with a short hash and message for quick scanning.

## 4. Git Fast-Forward Merge
*   **What it is:** A special type of merge that happens when your target branch (like `main`) hasn't changed since you created your feature branch.
*   **How it works:** Instead of creating a new "merge commit," Git simply moves the branch pointer forward to the tip of the feature branch.
*   **Command:** `git merge <feature-branch>` (happens automatically if no divergence exists).

## 5. Pulling Commits from Origin (`git pull`)
*   **What it does:** Fetches the latest commits from a remote repository (like GitHub) and automatically merges them into your current local branch.
*   **Command:** `git pull` (or `git pull origin <branch-name>`)
*   **Tip:** It is essentially a combination of `git fetch` followed by `git merge`.

## 6. `git merge`
*   **What it does:** Combines the history and code changes from a specified branch into your current active branch.
*   **Command:** `git merge <branch-name>`
*   **Example:** Switching to `main` and running `git merge feature-login` brings all login feature changes into `main`.

## 7. `git diff`
*   **What it does:** Shows you the exact line-by-line code changes (additions and deletions) that you have made but haven't committed yet.
*   **Common Variations:**
    *   `git diff` — Shows changes in your working directory that are **not yet staged**.
    *   `git diff --staged` (or `--cached`) — Shows changes that **are staged** and ready to be committed.
