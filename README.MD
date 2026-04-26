
# Resources & Further Reading

## Official & Core References
| # | Resource | Link |
|---|----------|------|
| 1 | Pro Git – free online book **(must read)** | https://git-scm.com/book/en/v2 |
| 2 | Git Basics **(must read)** | https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository |
| 3 | Git Reference Manual | https://git-scm.com/docs |
| 4 | GitHub Home Page | https://github.com/ |
| 5 | Git Download | https://git-scm.com/downloads |

## Interactive Courses & Videos
| # | Resource | Link |
|---|----------|------|
| 6 | Learn Git Branching (interactive) | https://learngitbranching.js.org/ |
| 7 | GitHub Skills (official courses) | https://skills.github.com/ |
| 8 | Atlassian Git Tutorials | https://www.atlassian.com/git/tutorials |
| 9 | Git Immersion (guided tour) | https://gitimmersion.com/ |
| 10 | Linus Torvalds on Git (Google Talk) | https://www.youtube.com/watch?v=4XpnKHJAok8 |

## Cheat Sheets & Quick References
| # | Resource | Link |
|---|----------|------|
| 11 | GitHub Git Cheat Sheet (PDF) | https://education.github.com/git-cheat-sheet-education.pdf |
| 12 | Atlassian Git Cheat Sheet | https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet |
| 13 | Tower Git Cheat Sheet | https://www.git-tower.com/blog/git-cheat-sheet |
| 14 | Visual Git Reference | https://marklodato.github.io/visual-git-guide/index-en.html |

## GUI Clients
| # | Resource | Link |
|---|----------|------|
| 15 | GitHub Desktop | https://desktop.github.com/ |
| 16 | Sourcetree (free) | https://www.sourcetreeapp.com/ |
| 17 | GitKraken | https://www.gitkraken.com/ |
| 18 | VS Code built-in Git | https://code.visualstudio.com/docs/sourcecontrol/overview |

## Community & Help
| # | Resource | Link |
|---|----------|------|
| 19 | Stack Overflow – git tag | https://stackoverflow.com/questions/tagged/git |
| 20 | Oh Shit, Git!? (common fixes) | https://ohshitgit.com/ |
| 21 | GIT How To (guided tutorial) | https://githowto.com/ |
| 22 | First Aid Git (FAQ) | https://firstaidgit.io/ |

> Search your browser for **"git tutorials"** to find many more resources.

---

# Setup Git

## 1. Verify Installation

```bash
git --version
git config --list
```

## 2. Configure User Info (Required)

```bash
git config --global user.name "Your Name"
git config --global user.email your@email.com
```

Verify:

```bash
git config user.name
git config user.email
```

---

# Git Basics

## Git has 3 states:

* **Working Directory** → where you edit files
* **Staging Area** → files prepared for commit
* **Repository (.git)** → committed snapshots

---

# Project: Project Monkey

## 1. Create Project Folder

```bash
mkdir projectmonkey
cd projectmonkey
```

## 2. Initialize Repository

```bash
git init
```

## 3. View Hidden Files

```bash
ls -la   # Mac/Linux
```

---

# Create First File

Create:

```bash
HelloMonkey.java
```

```java
public class HelloMonkey {
    public static void main(String[] args) {
        System.out.println("Welcome to Project Monkey");
    }
}
```

---

# Git Workflow

## 1. Check Status

```bash
git status
```

## 2. Stage File

```bash
git add HelloMonkey.java
```

## 3. Commit File

```bash
git commit -m "Initial Project Monkey Commit"
```

## 4. Verify

```bash
git status
```

---

# Modify & Add Files

## Create README

```bash
README.txt
```

Add:

```
Information about Project Monkey will go in this file.
```

## Modify Java File

Add comment:

```java
// This is the main file for Project Monkey
```

---

## Stage & Commit Changes

```bash
git add --all
git commit -m "Added README and updated HelloMonkey"
```

---

# View History

```bash
git log
```

Short version:

```bash
git log --pretty=oneline
```

---

# Remove File from Staging

```bash
git rm --cached junk.txt
```

---

# Branching & Merging

## Create New Repo

```bash
cd ..
git init websites
cd websites
```

---


---

## Track and Commit

```bash
git add index.html
git commit -m "Initial website commit"
```

---

## Create Branch

```bash
git branch feature1.0
git checkout feature1.0
```

---

## Make Changes (Feature Branch)

Add:

* Contact info
* Under construction message

Then:

```bash
git add index.html
git commit -m "Feature 1.0 updates"
```

---

## Switch Back to Master

```bash
git checkout master
```

Make different changes (ex: background color)

```bash
git add index.html
git commit -m "Updated master version"
```

---

## Merge Feature Branch

```bash
git merge feature1.0
```

---

# Git History & Navigation

View logs:

```bash
git log
```

View last commit:

```bash
git log -1
```

Checkout old version:

```bash
git checkout <commit-hash>
```

---

# GitHub Section

## 1. Create Repo on GitHub

* Name: `myfirstrepo`
* Public
* Initialize with README

---

## 2. Clone Repo

```bash
git clone <repo-url>
cd myfirstrepo
```

---

## 3. Modify README

Add:

```
Hello from my PC!
```

---

## 4. Commit & Push

```bash
git add .
git commit -m "Updated README from local"
git push <repo-url>
```

---

# Final Deliverable

* Take a screenshot of your **GitHub commit history**
* Upload to assignment dropbox

---

# Key Commands Summary

```bash
git init
git status
git add
git commit
git log
git branch
git checkout
git merge
git clone
git push
```

---

# Platform Differences: macOS vs Linux vs Windows

## Opening a Terminal / Shell

| Task | macOS | Linux | Windows (CMD) | Windows (PowerShell) | Windows (Git Bash) |
|------|-------|-------|---------------|----------------------|--------------------|
| Open terminal | Terminal / iTerm2 | Terminal / Konsole | `cmd` | `powershell` | Git Bash (ships with Git for Windows) |
| Default shell | `zsh` (macOS 10.15+) / `bash` | `bash` / `zsh` | `cmd.exe` | `pwsh` | `bash` |

## Navigation Commands

| Action | macOS / Linux (bash/zsh) | Windows CMD | Windows PowerShell |
|--------|--------------------------|-------------|--------------------|
| Print current directory | `pwd` | `cd` | `pwd` or `Get-Location` |
| List files | `ls` or `ls -la` | `dir` | `ls` or `Get-ChildItem` |
| Change directory | `cd folder` | `cd folder` | `cd folder` |
| Go up one level | `cd ..` | `cd ..` | `cd ..` |
| Go to home directory | `cd ~` | `cd ~` | `cd ~` or `cd $HOME` |
| Clear screen | `clear` | `clear` | `cls` |
| Create folder | `mkdir folder` | `mkdir folder` | `mkdir folder` |
| Delete file | `rm file.txt` | `rm file.txt` | `del file.txt` |
| Delete folder (recursive) | `rm -rf folder` | `rm -rf folder` | `rmdir /s /q folder` or `rm -r folder` (PS) |
| Create empty file | `touch file.txt` | `touch file.txt` | `type nul > file.txt` or `New-Item file.txt` (PS) |
| View file contents | `cat file.txt` | `cat file.txt` | `type file.txt` or `cat file.txt` (PS) |
| Open in VS Code | `code .` | `code .` | `code .` |

> **Tip (Windows):** Install **Git for Windows** (https://gitforwindows.org/) — it includes Git Bash, which gives you `bash`, `ls`, `touch`, `rm`, etc., making commands identical to macOS/Linux.

## Line Endings (Critical for Cross-Platform Teams)

```bash
# Windows → check out CRLF, commit LF (recommended when working cross-platform)
git config --global core.autocrlf true

# macOS / Linux → commit LF, never convert
git config --global core.autocrlf input

# View current setting
git config core.autocrlf
```

## File Paths in Git Commands

| Situation | macOS / Linux | Windows CMD / PowerShell |
|-----------|---------------|--------------------------|
| Forward slash in paths | `git add src/main.js` | `git add src/main.js` ← Git always uses `/` |
| Quotes with spaces | `git add "my file.js"` | `git add "my file.js"` |

> Git on Windows accepts `/` in all paths — never use `\` with git commands.

---

# Helpful Git Hints & Extra Commands

## Staging

```bash
git add .                        # stage all changes in current directory
git add -A                       # stage all changes in entire repo (additions, deletions, renames)
git add -p                       # interactively choose hunks to stage (very useful!)
git restore --staged <file>      # unstage a file (keep changes in working dir)
git restore <file>               # discard uncommitted changes to a file (destructive!)
```

## Committing

```bash
git commit -m "message"          # commit with inline message
git commit -am "message"         # stage tracked files AND commit in one step
git commit --amend               # edit the last commit message (before pushing)
git commit --amend --no-edit     # add staged changes to last commit, keep message
```

## Viewing History

```bash
git log                          # full log
git log --oneline                # compact one-line-per-commit view
git log --oneline --graph --all  # ASCII branch graph — great for visualising branches
git log -n 5                     # show last 5 commits only
git log --author="Name"          # filter by author
git log -- <file>                # show history for a specific file
git diff                         # unstaged changes
git diff --staged                # staged changes (what will be committed)
git diff <branch1>..<branch2>    # diff between two branches
git show <commit-hash>           # show changes introduced by a commit
```

## Branching

```bash
git branch                       # list local branches
git branch -a                    # list all branches (local + remote)
git branch <name>                # create a new branch
git checkout <name>              # switch to branch (classic syntax)
git switch <name>                # switch to branch (modern syntax, Git 2.23+)
git checkout -b <name>           # create AND switch in one step (classic)
git switch -c <name>             # create AND switch in one step (modern)
git branch -d <name>             # delete branch (safe — only if merged)
git branch -D <name>             # force-delete branch
git branch -m <old> <new>        # rename a branch
```

## Merging & Rebasing

```bash
git merge <branch>               # merge branch into current branch
git merge --no-ff <branch>       # always create a merge commit (preserves history)
git merge --abort                # cancel an in-progress conflicting merge
git rebase main                  # rebase current branch onto main
git rebase --abort               # cancel an in-progress rebase
git rebase -i HEAD~3             # interactive rebase — squash/edit last 3 commits
```

## Remote Operations

```bash
git remote -v                    # list remotes with URLs
git remote add origin <url>      # add a remote named origin
git remote set-url origin <url>  # change the URL of an existing remote
git fetch origin                 # download changes without merging
git pull                         # fetch + merge
git pull --rebase                # fetch + rebase (cleaner linear history)
git push origin <branch>         # push branch to remote
git push -u origin <branch>      # push AND set upstream tracking
git push --force-with-lease      # safer force push (checks remote hasn't changed)
git clone <url>                  # clone a repository
git clone <url> <folder>         # clone into a specific folder name
```

## Undoing Things

```bash
git revert <commit-hash>         # create a new commit that undoes a previous commit (safe)
git reset --soft HEAD~1          # undo last commit, keep changes staged
git reset --mixed HEAD~1         # undo last commit, keep changes unstaged (default)
git reset --hard HEAD~1          # undo last commit AND discard all changes (destructive!)
git clean -fd                    # remove untracked files and directories (destructive!)
git stash                        # temporarily save uncommitted changes
git stash pop                    # restore the most recent stash
git stash list                   # list all stashes
git stash drop stash@{0}         # delete a specific stash
```

## Tags

```bash
git tag                          # list all tags
git tag v1.0                     # create a lightweight tag on current commit
git tag -a v1.0 -m "Release"     # create an annotated tag with a message
git push origin v1.0             # push a specific tag to remote
git push origin --tags           # push all tags to remote
```

## Aliases (Time Savers)

Add these to your global config once and use them forever:

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.lg "log --oneline --graph --all"
git config --global alias.undo "reset --soft HEAD~1"
```

Then use:

```bash
git st          # → git status
git lg          # → pretty branch graph
git undo        # → undo last commit softly
```

## .gitignore Tips

```bash
# Create a .gitignore file in your project root
touch .gitignore   # macOS/Linux/Git Bash
# Windows CMD:  type nul > .gitignore

# Check what is being ignored
git status --ignored

# Force-add an ignored file (use sparingly)
git add -f <file>

# Stop tracking a file that is already committed
git rm --cached <file>
git commit -m "Stop tracking <file>"
```

**Common .gitignore patterns:**

```
node_modules/     # Node dependencies
.env              # Environment secrets — NEVER commit this
*.log             # Log files
dist/             # Build output
.DS_Store         # macOS folder metadata
Thumbs.db         # Windows thumbnail cache
*.class           # Java compiled files
target/           # Maven / Gradle build output
```

## Resolving Merge Conflicts

1. Git marks conflicts inside the file like this:

```
<<<<<<< HEAD
Your version of the line
=======
Their version of the line
>>>>>>> feature-branch
```

2. Edit the file — delete the conflict markers and keep what you want.
3. Then:

```bash
git add <conflicted-file>
git commit
```

## Quick Health Checks

```bash
git status                       # always run this first
git log --oneline -10            # see recent history at a glance
git remote -v                    # confirm remote URLs
git config --list                # confirm your name/email/settings
git branch -a                    # see all branches
```

---

