# MJ Command-Line — Documentation Hub

**Maintained by**: Sovereign Architect (MJ Ahmad)  
**Purpose**: To provide a step-by-step guide for deploying MJ smart contracts to Mainnet or Testnet environments

---

## 🏆 Daily Git Essentials

### `Commands`
1. **Initialize a repo**  
   `git init` — start a new repository.

2. **Clone a repo**  
   `git clone <url>` — copy an existing repository.

3. **Stage changes**  
   `git add <file>` or `git add .` — prepare files for commit.

4. **Commit changes**  
   `git commit -m "message"` — save changes with a message.

5. **Switch branches**  
   `git switch <branch>` — move between branches.

6. **Create a branch**  
   `git switch -c <branch>` — start a new branch.

7. **View history**  
   `git log --oneline` — see a compact commit history.

8. **Compare changes**  
   `git diff` — check differences before committing.

9. **Push changes**  
   `git push origin main` — send commits to remote.

10. **Pull updates**  
    `git pull` — fetch and merge changes from remote.

---

**Initialize GitHub repo**

1. `git init`
2. `git add .`
3. `git commit -m "Initial commit"`
4. `git branch -M main`
5. `git remote add origin https://github.com/<your-username>/<repo-name>.git`
6. `git push -u origin main`
7. 


## Git Cheat Sheet

### 🔑 Main Points
- **Getting Started**
  - Initialize a repository: `git init`
  - Clone an existing repository: `git clone <url>`

- **Prepare to Commit**
  - Stage files: `git add <file>` or `git add .`
  - Remove or move files: `git rm`, `git mv`
  - Unstage changes: `git reset`

- **Make Commits**
  - Commit with a message: `git commit -m "message"`
  - Commit staged + tracked changes: `git commit -am "message"`

- **Branching**
  - Switch branches: `git switch <branch>` or `git checkout <branch>`
  - Create new branch: `git switch -c <branch>`
  - Delete branch: `git branch -d <branch>` (force with `-D`)

- **Diff & History**
  - Compare changes: `git diff`
  - Show commit details: `git show <commit>`
  - View logs: `git log`, `git log --oneline`
  - Blame file lines: `git blame <file>`

- **Undo & Restore**
  - Discard changes: `git restore <file>` or `git reset --hard`
  - Stash changes: `git stash`
  - Amend last commit: `git commit --amend`

- **Merge & Rebase**
  - Merge branches: `git merge`
  - Rebase: `git rebase`
  - Cherry-pick commits: `git cherry-pick <commit>`

- **Remote Operations**
  - Add remote: `git remote add <name> <url>`
  - Push changes: `git push origin main`
  - Pull changes: `git pull`

- **Configuration**
  - Set username/email: `git config user.name "Name"`, `git config user.email "Email"`
  - Global config: `git config --global ...`
  - Aliases: `git config alias.st status`

- **Important Files**
  - Local config: `.git/config`
  - Global config: `~/.gitconfig`
  - Ignore list: `.gitignore`  

---

👉 These ten cover the **core workflow**: start a repo, make changes, commit, branch, review, and sync with remotes.  

Next, create a **visual workflow diagram** showing how these commands connect in a typical project cycle