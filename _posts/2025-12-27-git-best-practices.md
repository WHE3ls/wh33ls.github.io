---
layout: post
title: "Git Best Practices for Tech Notes"
date: 2025-12-27 00:00:00 +0000
categories: [git, best-practices]
tags: [git, version-control, workflow]
---

Git is an essential tool for any developer. Here are some best practices I follow when managing my tech notes and code repositories.

## Commit Messages

Write clear, descriptive commit messages that explain *what* and *why*:

### Good Examples

```bash
git commit -m "Add authentication middleware for API routes"
git commit -m "Fix memory leak in image processing pipeline"
git commit -m "Update README with installation instructions"
```

### Poor Examples

```bash
git commit -m "fixed stuff"
git commit -m "updates"
git commit -m "asdf"
```

## Commit Often, Push Regularly

- Make small, focused commits
- Each commit should represent a logical unit of work
- Push to remote regularly to backup your work

## Branching Strategy

Use branches for different features or experiments:

```bash
# Create a new branch
git checkout -b feature/new-blog-post

# Work on your changes
git add .
git commit -m "Add new blog post about Docker"

# Push branch to remote
git push origin feature/new-blog-post
```

## Keep Your History Clean

Before merging, consider cleaning up your commit history:

```bash
# Interactive rebase to squash or edit commits
git rebase -i HEAD~3
```

## Use .gitignore

Always include a `.gitignore` file to exclude:

- Build artifacts
- Dependencies (node_modules, vendor)
- IDE-specific files
- Environment files with secrets
- OS-specific files (.DS_Store)

Example `.gitignore`:

```
# Dependencies
node_modules/
vendor/

# Build outputs
dist/
build/
_site/

# Environment files
.env
.env.local

# IDE
.vscode/
.idea/

# OS
.DS_Store
Thumbs.db
```

## Review Changes Before Committing

Always review your changes:

```bash
# See what's changed
git status
git diff

# Stage specific files
git add specific-file.js

# Review staged changes
git diff --staged
```

## Key Takeaways

1. Write meaningful commit messages
2. Commit frequently, push regularly
3. Use branches for features and experiments
4. Keep sensitive data out of version control
5. Review changes before committing

## Useful Git Commands

```bash
# Undo last commit (keep changes)
git reset --soft HEAD~1

# Discard local changes
git checkout -- filename

# View commit history
git log --oneline --graph

# Stash changes temporarily
git stash
git stash pop
```

Following these practices will make your Git workflow smoother and your repository history more maintainable!
