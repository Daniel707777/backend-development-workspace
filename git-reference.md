# Git Command Cheat Sheet

## Start here

```bash
git status
git log --oneline
git diff
```

Use `git status` often to see the current branch and which files are modified, staged, or untracked.

## Make and review changes

```bash
git add <file>                 # Stage a specific file
git add .                      # Stage changes in the current directory
git diff                       # Review unstaged changes
git diff --staged              # Review staged changes
git restore <file>             # Discard unstaged changes to a file
git restore --staged <file>    # Unstage a file, keeping its changes
```

Review a diff before staging or committing. `git restore <file>` discards work, so use it only when that is intentional.

## Commit changes

```bash
git commit -m "Describe the change"
git show --stat                # Review the latest commit summary
git log --oneline --graph      # View commit history
```

Write short commit messages that describe the change.

## Branches

```bash
git branch                     # List local branches
git switch -c <branch-name>    # Create and switch to a branch
git switch <branch-name>       # Switch branches
git branch -d <branch-name>    # Delete a merged local branch
```

Commit or otherwise preserve your work before switching branches.

## Remotes and sharing

```bash
git remote -v                  # Show configured remotes
git fetch                      # Download remote updates without merging
git pull                       # Fetch and integrate the current branch's upstream
git push -u origin <branch>    # Publish a branch and set its upstream
git push                       # Push commits to the configured upstream
```

Fetch and review remote changes before integrating them when you need more control than `git pull` provides.

## Temporarily set changes aside

```bash
git stash push -m "Short description"
git stash list
git stash apply                # Restore the latest stash and keep it in the list
git stash pop                  # Restore and remove the latest stash
```

Check `git status` after restoring a stash, since the changes may need attention or conflict resolution.
