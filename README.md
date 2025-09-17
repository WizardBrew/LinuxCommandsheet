#!/usr/bin/env bash
# -----------------------------------------------------------------------------
# generate-git-cheatsheet.sh
# A one-shot script to create “git_cheat_sheet.md” in your current directory.
# Just copy, paste, chmod +x, and run.
# -----------------------------------------------------------------------------

cat << 'EOF' > git_cheat_sheet.md
# Git Command Cheat Sheet

A concise, copy-paste-ready Markdown guide to get you up and running with Git, 
from initial setup through branching, committing, remote workflows, and advanced tips.

---

## 🔧 Configuration

| Command                                               | Description                     |
|-------------------------------------------------------|---------------------------------|
| `git config --global user.name "Your Name"`           | Set your global username        |
| `git config --global user.email "you@example.com"`    | Set your global email           |
| `git config --global core.editor "vim"`               | Choose default commit editor    |
| `git config --global alias.st status`                 | Create `git st` alias for status|

---

## 📂 Repository Initialization & Cloning

| Command                                 | Description                                   |
|-----------------------------------------|-----------------------------------------------|
| `git init`                              | Initialize a new repository                   |
| `git clone <url>`                       | Clone an existing repository                  |
| `git clone -b <branch> <url> <folder>`  | Clone a specific branch into a folder         |

---

## 📝 Staging & Committing

| Command                                   | Description                                |
|-------------------------------------------|--------------------------------------------|
| `git status`                              | Show working tree status                   |
| `git add <file>`                          | Stage a file                               |
| `git add .`                               | Stage all changed files                    |
| `git commit -m "message"`                 | Create a commit                            |
| `git commit --amend --no-edit`            | Amend last commit without changing message |
| `git reset HEAD <file>`                   | Unstage a file                             |

---

## 🌿 Branching & Merging

| Command                                 | Description                                     |
|-----------------------------------------|-------------------------------------------------|
| `git branch`                            | List all branches                               |
| `git branch <name>`                     | Create a new branch                             |
| `git checkout <name>`                   | Switch to a branch                              |
| `git checkout -b <name>`                | Create & switch to new branch                   |
| `git merge <branch>`                    | Merge a branch into current                     |
| `git branch -d <branch>`                | Delete a local branch                           |

---

## 🔄 Rebasing & Reset

| Command                                         | Description                                    |
|-------------------------------------------------|------------------------------------------------|
| `git rebase <branch>`                           | Reapply commits on top of another branch       |
| `git rebase --interactive <hash>`               | Edit, reorder, squash commits                  |
| `git reset --soft HEAD~1`                       | Undo last commit, keep changes staged          |
| `git reset --hard HEAD~1`                       | Undo last commit and discard changes           |

---

## 🌐 Remote Repositories

| Command                                      | Description                                      |
|----------------------------------------------|--------------------------------------------------|
| `git remote -v`                              | List configured remotes                          |
| `git remote add origin <url>`                | Add a new remote named `origin`                  |
| `git fetch`                                  | Download objects and refs from remote            |
| `git pull`                                   | Fetch + merge remote changes into current branch |
| `git push`                                   | Push commits to default remote and branch        |
| `git push -u origin <branch>`                | Push & set upstream                              |

---

## 📦 Tagging & Releases

| Command                                | Description                           |
|----------------------------------------|---------------------------------------|
| `git tag`                              | List tags                             |
| `git tag <name>`                       | Create lightweight tag                |
| `git tag -a <name> -m "msg"`           | Create annotated tag                  |
| `git push --tags`                      | Push all tags to remote               |

---

## 🔍 Inspection & History

| Command                                     | Description                              |
|---------------------------------------------|------------------------------------------|
| `git log`                                   | Show commit history                      |
| `git log --oneline --graph --all`           | Condensed, graphical view                |
| `git show <commit>`                         | Show changes of a specific commit        |
| `git diff`                                  | Show unstaged changes                    |
| `git diff --staged`                         | Show staged changes                      |

---

## 🛠️ Undo & Cleanup

| Command                                   | Description                             |
|-------------------------------------------|-----------------------------------------|
| `git restore <file>`                      | Discard changes in working directory    |
| `git clean -fd`                           | Remove untracked files and directories  |
| `git stash`                               | Stash changes                           |
| `git stash pop`                           | Reapply stashed changes                 |
| `git stash list`                          | List stashed entries                    |

---

## 💡 Tips & Best Practices

- Use descriptive commit messages:  
  ‣ Start with a verb (e.g., “Add”, “Fix”, “Refactor”)  
  ‣ Reference related issues or tickets  
- Adopt a branching strategy (Git Flow, GitHub Flow) to keep your workflow organized.  
- Configure useful aliases in your `~/.gitconfig` for repetitive commands.  
- Regularly `git fetch` and rebase to minimize merge conflicts on long-lived branches.  

---

### More Resources

- Official Git Book: https://git-scm.com/book  
- Interactive Tutorial: https://learngitbranching.js.org/  
- Git Tips & Tricks: https://github.com/git-tips/tips
EOF

echo "✅ git_cheat_sheet.md has been generated in $(pwd)"
