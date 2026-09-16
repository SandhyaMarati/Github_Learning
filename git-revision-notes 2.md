# Git/GitHub Revision — Full Flow

## Setup (one-time only)
```
git --version                          → check Git is installed
git config --global user.name "..."    → set your name for commits
git config --global user.email "..."   → set your email for commits
```

## Start a project & first push
```
git init                               → start tracking this folder with Git
git add .                              → stage all changed files (ready to save)
git commit -m "message"                → save a permanent snapshot locally
git branch -M main                     → name the main branch "main"
git remote add origin <github-url>     → link local repo to GitHub repo
git push -u origin main                → upload local commits to GitHub
```

## Daily loop (repeat this after any edit)
```
git status                             → see what changed / staged / not staged
git diff <file>                        → see exact line-by-line changes before committing
git add .                              → stage changes
git commit -m "message"                → save snapshot
git push                               → upload to GitHub
```

## Viewing history
```
git log --oneline                      → list all commits (short form) = "all versions"
```

## Branches (isolate experimental work)
```
git branch                             → list branches, * shows current one
git checkout -b <branch-name>          → create + switch to a new branch
git status                             → confirm you're "on branch <name>"
git add . / git commit -m "..."        → commit changes onto THIS branch only
git checkout main                      → switch back to main (branch's changes disappear temporarily)
git merge <branch-name>                → bring that branch's changes into main
git push                               → upload the merged main to GitHub
git branch -d <branch-name>            → delete branch once merged (optional cleanup)
```

## Cloning & syncing across machines
```
git clone <github-url>                 → download a full copy of a repo (first time only)
git log --oneline                      → confirm full commit history came with it
git pull                                → download any NEW commits pushed by anyone since last check
```

## The 3-role mental model
- **Working directory** → your files as you edit them
- **Staging area** → files marked "ready to save" (`git add`)
- **Local repo** → saved snapshots on your machine (`git commit`)
- **GitHub (remote)** → online copy (`git push` sends here, `git pull`/`git clone` bring from here)

## Quick command index (memorize these 8)
```
git status
git diff
git add .
git commit -m "..."
git push
git pull
git branch / git checkout -b <name>
git merge <name>
```
