# Git and GitHub Learning Progress

## Goal

Learn to track code changes, maintain repositories, and publish my work on GitHub confidently.

## 1. Repository Basics

**Status:** Practiced

- Created a GitHub repository named `coding-journey`.
- Cloned the repository onto my computer.
- Worked with files and folders inside the local repository.
- Used GitHub to store my learning documentation.

## 2. Commands Practiced

### Check repository status

```bash
git status
```

Shows changed, staged, and untracked files.

### Stage changes

```bash
git add README.md
```

Stages a specific file for the next commit.

To stage all changes:

```bash
git add .
```

Review the staged changes before committing.

### Commit changes

```bash
git commit -m "Update learning progress"
```

Records staged changes in the local Git repository.

### Push changes

```bash
git push
```

Uploads local commits to the configured remote repository.

## 3. `.gitignore`

**Status:** Practiced

Learned why generated files and local environments should generally not be committed.

Examples:

```gitignore
.venv/
__pycache__/
*.pyc
```

## 4. GitHub Workflow

My usual workflow:

1. Edit or create files.
2. Run `git status`.
3. Review the changes.
4. Stage the intended files.
5. Commit with a meaningful message.
6. Push to GitHub.
7. Check the repository online.

## 5. Skills to Learn Next

- [ ] `git diff` to inspect changes.
- [ ] `git log` to inspect commit history.
- [ ] `git pull` to fetch and integrate remote changes.
- [ ] Create and switch branches.
- [ ] Merge branches.
- [ ] Resolve merge conflicts.
- [ ] Understand remotes and upstream branches.
- [ ] Improve commit messages.
- [ ] Write useful project READMEs.

## Important Lessons

- A commit records changes locally; it does not automatically upload them.
- A push sends local commits to the remote repository.
- `.gitignore` prevents matching untracked files from being added normally, but does not automatically remove files already tracked by Git.
- Review `git status` before staging and committing.
- Never commit passwords, API keys, or other secrets.

## Next Step

Continue documenting my learning journey, then practice `git diff` and `git log` to understand my changes and commit history.