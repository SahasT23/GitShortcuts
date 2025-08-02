# TestProject
# 🧠 Ultimate Git Command Reference

---

## 🪜 Basics & Setup
- `git config --global user.name "Your Name"`
- `git config --global user.email "you@example.com"`
- `git config --list`
- `git init`
- `git clone <repo-url>`
- `git status`
- `git add <file>`
- `git add .`
- `git commit -m "Your message"`
- `git push`
- `git pull`
- `git fetch`

---

## 🌿 Branching & Merging
- `git branch`
- `git branch <new-branch>`
- `git checkout <branch>`
- `git switch <branch>`
- `git merge <branch>`
- `git rebase <branch>`
- `git rebase -i HEAD~n`
- `git merge --no-ff <branch>`

---

## 📍 Staging, Stashing & Undo
- `git reset <file>`
- `git reset --soft HEAD~1`
- `git reset --mixed HEAD~1`
- `git reset --hard HEAD~1`
- `git stash`
- `git stash -p`
- `git stash pop`
- `git restore --source=<branch> <file>`
- `git restore --staged <file>`
- `git checkout -- <file>`
- `git checkout <commit> -- <path>`

---

## 📦 Remote Repositories
- `git remote -v`
- `git remote add origin <repo-url>`
- `git push -u origin <branch>`
- `git push origin :branch-name`

---

## 🧾 Logs, History & Diff
- `git log`
- `git log --oneline`
- `git log --graph --oneline --all`
- `git log --pretty=format:"%h - %s (%cr)"`
- `git log --author="name"`
- `git log -p`
- `git log -S 'keyword'`
- `git log --show-signature`
- `git shortlog -sn`
- `git show <commit>`
- `git reflog`
- `git reflog show HEAD@{n}`
- `git diff`
- `git diff --cached`
- `git diff HEAD~3..HEAD --stat`
- `git diff --word-diff`
- `git diff <file>`

---

## 🔍 Search & Blame
- `git blame <file>`
- `git grep 'term'`
- `git grep -n 'def ' -- '*.py'`
- `git grep -e 'pattern' --and -e 'other-pattern'`

---

## 🧪 Commit & History Editing
- `git commit --amend`
- `git cherry-pick <commit>`
- `git cherry-pick -n <commit>`
- `git rebase -x 'command'`
- `git rebase --onto <newbase> <upstream> <branch>`
- `git revert <commit>`
- `git filter-branch --tree-filter 'rm -f secret.txt' HEAD`
- `git replace <old> <new>`

---

## 📂 File Operations
- `git rm <file>`
- `git mv <old> <new>`

---

## 🧠 Git Aliases
- `git config --global alias.co checkout`
- `git config --global alias.br branch`
- `git config --global alias.ci commit`
- `git config --global alias.st status`

---

## 🧬 Git Internals & Refs
- `git rev-parse HEAD`
- `git rev-parse --short HEAD`
- `git cat-file -t <hash>`
- `git cat-file -p <hash>`
- `git ls-tree HEAD`
- `git show-ref`
- `git for-each-ref`
- `git update-ref <ref> <commit>`

---

## 🧩 Git Worktree
- `git worktree add ../feature-branch feature-branch`
- `git worktree add --detach ../dir`
- `git worktree list`
- `git worktree remove ../feature-branch`
- `git worktree prune`

---

## 🔒 Credential & Signing
- `git config --global commit.gpgSign true`
- `git commit -S -m "Signed commit"`
- `git verify-commit <commit>`
- `git push --signed`
- `git credential-store`
- `git credential-cache`
- `git credential-manager`

---

## 🧙 Git Hooks (in `.git/hooks`)
- `pre-commit`
- `commit-msg`
- `post-checkout`
- `post-merge`
- Make executable with: `chmod +x hook-name`

---

## 🧮 Statistics & Cleanup
- `git diff --numstat`
- `git branch --sort=-committerdate`
- `git gc`
- `git fsck`
- `git prune`

---

## 🧪 Git Bisect
- `git bisect start`
- `git bisect good <commit>`
- `git bisect bad`
- `git bisect reset`
- `git bisect run python test_script.py`

---

## 🌐 Collaboration Tools
- `.mailmap` — Normalize contributor names/emails in logs
- `git tag`
- `git tag -a <tag> -m "message"`

---

## 🎁 Archiving & Portability
- `git archive --format=zip HEAD > latest.zip`
- `git bundle create repo.bundle HEAD master`
- `git bundle verify <file>`
- `git bundle list-heads <file>`
- `git clone repo.bundle -b master repo-clone`
- `git fast-export`
- `git fast-import`

---

## 📌 Git Daemon & Instaweb
- `git daemon --reuseaddr --base-path=. --export-all`
- `git instaweb`

---

## 🛡️ Global Ignore
- Create: `~/.gitignore_global`
- Set: `git config --global core.excludesFile ~/.gitignore_global`

---

## 🔀 Workflow Models
- **Gitflow** — Feature branches + develop/master strategy  
- **GitHub Flow** — Simple branching and PRs on main  
- **Trunk-based** — All commits go into a single main branch, frequent integration

### Useful Commands for Flow Management:
- `git checkout -b feature/<name>`  
- `git checkout -b hotfix/<issue>`  
- `git merge develop`  
- `git push origin release/<version>`  

---

## 🔧 Advanced Git Configuration
- `git config --global pull.rebase true` — Default pull to rebase  
- `git config --global core.editor "vim"` — Set default editor  
- `git config --global core.autocrlf input` — Normalize line endings  
- `git config --global init.defaultBranch main` — Set default branch name  

---

## 📁 Directory-Level Strategies
- `.gitignore` — Ignore files/folders  
- `.gitattributes` — Define file handling rules (e.g., binary vs text)  
- `.gitmodules` — Track submodules configuration  
- `.mailmap` — Normalize author names/emails  

---

## 🚦 Status & Tracking Precision
- `git status -s` — Short format  
- `git diff --name-status` — Changes by file name and type  
- `git diff --check` — Find whitespace errors  

---

## ⚙️ Server & Network Utilities
- `git daemon --reuseaddr` — Serve repo locally  
- `git update-server-info` — Prepares repository for HTTP transport  
- `git remote show origin` — Details on origin sync  

---

## 🧬 Object Storage & Packfile Insights
- `git count-objects -v` — Count loose objects  
- `git verify-pack -v .git/objects/pack/*.idx` — Inspect packfile  
- `git unpack-objects < pack-file` — Manual unpacking  

---

## 🔁 Rebasing Tactics
- `git rebase --preserve-merges` — Keep merge commits  
- `git rebase --root` — Rewrite entire history from first commit  
- `git rebase --skip` — Skip problem commits during rebase  
- `git rebase --continue` — Resume interrupted rebase  

---

## 💼 Interactive Additions
- `git add -i` — Interactive add UI  
- `git clean -df` — Remove untracked files/folders  
- `git clean -xdf` — Remove all ignored/untracked content  

---

## 📊 Contribution Insights
- `git fame` (via plugin) — Contributor stats  
- `git log --numstat --pretty="%an"` — Author contribution by lines  
- `git shortlog -e` — Emails + commit counts  

---

## 🌎 International & Encoding Configs
- `git config --global i18n.commitEncoding utf-8`  
- `git config --global i18n.logOutputEncoding utf-8`  

---

## 🧠 Git Notes
- `git notes add -m "Extra info"` — Annotate commits  
- `git notes show <commit>` — View notes  
- `git log --show-notes` — Display with history  

---
