# Git Commands Guide

## Basic Repository Setup

```shell
# Initialize a new Git repository
git init

# Create a new README file
echo "# Project-Name" >> README.md

# Add all files to staging
git add .

# Commit changes with a message
git commit -m "first commit"

# Add remote repository
git remote add origin git@github.com:username/repository.git

# Rename default branch to main
git branch -M main

# Push changes to remote repository
git push -u origin main

# Remove remote repository
git remote remove origin
```

## Common Git Operations

```shell
# Check repository status
git status

# View commit history
git log

# Pull changes from remote
git pull origin main

# Force pull (discard local changes)
git fetch origin
git reset --hard origin/main

# Create and switch to a new branch
git checkout -b feature/new-feature

# Switch to an existing branch
git checkout branch-name

# Merge a branch into current branch
git merge branch-name

# Delete a branch
git branch -d branch-name
```

## Advanced Operations

```shell
# Stash changes temporarily
git stash

# Apply stashed changes
git stash pop

# View all remote repositories
git remote -v

# Update remote URL
git remote set-url origin new-url

# Revert last commit
git revert HEAD

# Reset to a specific commit
git reset --hard commit-hash

# Force push (use with caution)
git push -f origin main
```

## Configuration

```shell
# Set global username
git config --global user.name "Your Name"

# Set global email
git config --global user.email "your.email@example.com"

# View current configuration
git config --list
```

## Tips
- Always commit with meaningful messages
- Use branches for new features
- Pull before pushing to avoid conflicts
- Be careful with force push and force pull operations
- Keep your repository clean and organized
