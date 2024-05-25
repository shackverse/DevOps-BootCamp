### Git 



## What Is Git?

**Git** is a distributed version control system used to track changes in source code during software development. It allows multiple developers to work on the same project efficiently and without interfering with each other's work.

**Example**:
- Tracking changes in a project
- Collaborative development



## Git VS GitHub

**Git**:
- A version control system to manage code history.
- Operates locally on your machine.
  
**GitHub**:
- A web-based platform for hosting Git repositories.
- Facilitates collaboration and sharing.

**Example**:
- Git: Keeping track of changes locally.
- GitHub: Sharing a project with team members.



## Create Repo

### Creating a Local Repository

1. Initialize a new repository:
   ```bash
   git init myproject
   cd myproject
   ```

### Creating a Repository on GitHub

1. Go to [GitHub](https://github.com) and log in.
2. Click on the '+' icon in the top-right corner and select 'New repository'.
3. Fill in the repository details and click 'Create repository'.



## Personal Access Token in GitHub

### Creating a Personal Access Token

1. Go to [GitHub Settings](https://github.com/settings/tokens).
2. Click on 'Generate new token'.
3. Select scopes and click 'Generate token'.
4. Copy the token (you won't see it again).

### Using the Token

When prompted for a password during Git operations, use the token instead.

**Example**:
```bash
git clone https://github.com/username/repo.git
# When prompted for password, paste your personal access token.
```



## Clone Repo on Local & Git Commands

### Cloning a Repository

1. Clone a repository to your local machine:
   ```bash
   git clone https://github.com/username/repo.git
   cd repo
   ```

### Common Git Commands

- **Status**: Check the status of your repository.
  ```bash
  git status
  ```
- **Add**: Stage changes for commit.
  ```bash
  git add .
  ```
- **Commit**: Commit staged changes.
  ```bash
  git commit -m "Commit message"
  ```
- **Push**: Push changes to the remote repository.
  ```bash
  git push
  ```



## Branches in Git [Create/Manage/Delete] & Git Fetch VS Pull

### Branch Management

- **Create a new branch**:
  ```bash
  git branch new-feature
  ```
- **Switch to a branch**:
  ```bash
  git checkout new-feature
  ```
- **Delete a branch**:
  ```bash
  git branch -d new-feature
  ```

### Fetch vs. Pull

- **Fetch**: Fetches updates from the remote repository but doesn't merge them.
  ```bash
  git fetch
  ```
- **Pull**: Fetches and merges updates from the remote repository.
  ```bash
  git pull
  ```



## Git Merge VS Rebase

### Merge

- Combines changes from one branch into another.
  ```bash
  git merge feature-branch
  ```

### Rebase

- Reapplies commits on top of another base tip.
  ```bash
  git checkout feature-branch
  git rebase master
  ```

**Example**:
- **Merge**: Keeps all commit history.
- **Rebase**: Creates a linear history.



## Git Stash & Pop

### Stash

- Temporarily saves changes without committing.
  ```bash
  git stash
  ```

### Pop

- Applies stashed changes and removes them from stash.
  ```bash
  git stash pop
  ```

**Example**:
- **Stash**: Switching branches without committing work-in-progress.
- **Pop**: Returning to your work after switching back.



## Git Branching Strategies

### Strategies

- **Mainline (Trunk) Development**: All developers commit to the main branch.
- **Feature Branching**: Each feature is developed in its own branch.
- **Gitflow**: Uses multiple branches for feature, release, and hotfix.

**Example**:
- **Feature Branching**: Developers work on new features in separate branches and merge them when complete.
- **Gitflow**: Structured approach with separate branches for development, features, and releases.


