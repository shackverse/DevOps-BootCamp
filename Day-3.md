# DAY-3 | Git 

**Git** is a distributed version control system that helps developers manage and track changes in their codebase efficiently. It was created by Linus Torvalds in 2005 to handle the development of the Linux kernel. Git allows multiple developers to work on a project simultaneously without overwriting each other's changes.

#### Key Features of Git:
- **Distributed Version Control:** Every developer has a complete copy of the project history.
- **Branching and Merging:** Easy to create, manage, and merge branches.
- **Lightweight:** Efficient with minimal overhead.
- **Speed:** Designed for performance and large projects.

#### Example Commands:
1. **Initialize a Git repository:**
   ```bash
   git init
   ```
   This command initializes a new Git repository in the current directory.

2. **Add files to staging area:**
   ```bash
   git add filename
   git add .
   ```
   Adds specified files or all changes in the working directory to the staging area.

3. **Commit changes:**
   ```bash
   git commit -m "Initial commit"
   ```
   Records the changes in the repository with a message.

4. **Check status:**
   ```bash
   git status
   ```
   Shows the status of the working directory and staging area.

5. **View commit history:**
   ```bash
   git log
   ```
   Displays the commit history.

### Git vs. GitHub

**GitHub** is a web-based platform that provides Git repository hosting. While Git is a version control system, GitHub is a cloud-based service for hosting Git repositories, enabling collaborative development and offering additional features like issue tracking, code review, and project management.

#### Key Differences:
- **Git:** A version control system to manage and track changes in your codebase.
- **GitHub:** A platform to host Git repositories and collaborate with other developers.

#### Example Scenario:
Imagine you and a friend are working on a project together. Here's how Git and GitHub facilitate collaboration:

1. **Initialize a Git Repository Locally:**
   ```bash
   git init myproject
   cd myproject
   ```

2. **Create a GitHub Repository:**
   - Go to GitHub and create a new repository named `myproject`.

3. **Connect Local Repository to GitHub:**
   ```bash
   git remote add origin https://github.com/yourusername/myproject.git
   git branch -M main
   git push -u origin main
   ```
   This links your local repository to the GitHub repository and pushes the initial commit.

4. **Clone a Repository:**
   If your friend wants to collaborate, they can clone the repository:
   ```bash
   git clone https://github.com/yourusername/myproject.git
   cd myproject
   ```

5. **Create a New Branch:**
   ```bash
   git checkout -b feature-branch
   ```

6. **Make Changes and Commit:**
   ```bash
   echo "New feature" > feature.txt
   git add feature.txt
   git commit -m "Added new feature"
   ```

7. **Push Changes to GitHub:**
   ```bash
   git push origin feature-branch
   ```

8. **Create a Pull Request:**
   On GitHub, your friend can create a pull request to merge `feature-branch` into `main`.

9. **Merge the Pull Request:**
   Once reviewed, the pull request can be merged, incorporating the changes into the main branch.

### Real-Time Example

Let's say you're working on a website project. You want to add a new feature without affecting the main codebase. Using Git and GitHub, you can create a separate branch, work on the feature, and then merge it once it's ready.

1. **Create a New Branch:**
   ```bash
   git checkout -b add-new-feature
   ```

2. **Make Changes:**
   Edit files and implement the new feature.

3. **Stage and Commit Changes:**
   ```bash
   git add .
   git commit -m "Implemented new feature"
   ```

4. **Push Changes to GitHub:**
   ```bash
   git push origin add-new-feature
   ```

5. **Create a Pull Request on GitHub:**
   Go to the GitHub repository, navigate to the "Pull Requests" tab, and create a new pull request for `add-new-feature`.

6. **Review and Merge:**
   Review the changes and merge the pull request once everything looks good.

By following these steps, you can efficiently manage your project using Git and GitHub, ensuring smooth collaboration and version control.

### Summary

- **Git:** Distributed version control system for tracking changes in code.
- **GitHub:** Platform for hosting Git repositories and collaborating on code.


####  **Personal Access Token in GitHub**

**What is a Personal Access Token?**

A Personal Access Token (PAT) is an alternative to using passwords for authentication to GitHub when using the GitHub API or the command line. It's more secure and recommended, especially for accessing your repositories via command-line tools.

**Steps to Create a Personal Access Token:**

1. **Log in to GitHub:**
   Go to [GitHub](https://github.com) and log in to your account.

2. **Navigate to Settings:**
   Click on your profile picture in the upper-right corner, then select "Settings."

3. **Access Developer Settings:**
   Scroll down to "Developer settings" in the left-hand menu.

4. **Generate New Token:**
   Go to "Personal access tokens" and click "Generate new token."

5. **Select Scopes:**
   Choose the scopes or permissions you need. For most repository-related tasks, select `repo`.

6. **Generate Token:**
   Click "Generate token" at the bottom of the page.

7. **Copy and Store:**
   Copy the generated token and store it securely. You won't be able to see it again.

**Using Personal Access Token:**

When prompted for a password in the terminal, use the token instead.

```bash
git clone https://github.com/username/repo.git
Username: your_username
Password: your_personal_access_token
```

#### **Clone Repo on Local & Git Commands**

**Cloning a Repository:**

```bash
git clone https://github.com/username/repo.git
```

**Example:**

```bash
git clone https://github.com/octocat/Hello-World.git
cd Hello-World
```

**Basic Git Commands:**

- **Initialize a repository:**

  ```bash
  git init
  ```

- **Check status:**

  ```bash
  git status
  ```

- **Add files to staging area:**

  ```bash
  git add file1.txt file2.txt
  ```

- **Commit changes:**

  ```bash
  git commit -m "Initial commit"
  ```

- **Push to remote repository:**

  ```bash
  git push origin main
  ```

#### **Git Fetch vs. Pull**

**Git Fetch:**

`git fetch` downloads commits, files, and references from a remote repository into your local repository. However, it does not merge these changes into your working directory.

**Example:**

```bash
git fetch origin
```

**Git Pull:**

`git pull` is a combination of `git fetch` and `git merge`. It fetches changes from the remote repository and immediately tries to merge them into the current branch.

**Example:**

```bash
git pull origin main
```

**Difference:**

- **Fetch:** Retrieves changes but does not apply them.
- **Pull:** Retrieves and applies changes to the working directory.

####  **Branches in Git (Create/Manage/Delete)**

**Creating a Branch:**

```bash
git branch new-feature
```

**Switching to a Branch:**

```bash
git checkout new-feature
```

Or using the combined command:

```bash
git checkout -b new-feature
```

**Managing Branches:**

- **List all branches:**

  ```bash
  git branch
  ```

- **Rename a branch:**

  ```bash
  git branch -m old-branch-name new-branch-name
  ```

- **Merge branches:**

  ```bash
  git checkout main
  git merge new-feature
  ```

**Deleting a Branch:**

- **Delete a local branch:**

  ```bash
  git branch -d new-feature
  ```

- **Delete a remote branch:**

  ```bash
  git push origin --delete new-feature
  ```

**Real-Time Example Workflow:**

1. **Create and switch to a new branch:**

   ```bash
   git checkout -b feature-login
   ```

2. **Work on the new feature and commit changes:**

   ```bash
   git add .
   git commit -m "Add login feature"
   ```

3. **Push the new branch to remote:**

   ```bash
   git push origin feature-login
   ```

4. **Create a pull request on GitHub and merge it into `main`.**

5. **Delete the feature branch after merging:**

   ```bash
   git branch -d feature-login
   git push origin --delete feature-login
   ```

#### Git Merge vs. Rebase

**Git Merge:**
Merging is a way to combine the changes from one branch into another. It is typically used to integrate the changes from a feature branch into the main branch (e.g., `main` or `master`).

**Example:**
1. **Create and switch to a new branch:**
   ```bash
   git checkout -b feature-branch
   ```

2. **Make changes and commit them:**
   ```bash
   echo "New feature" >> feature.txt
   git add feature.txt
   git commit -m "Add new feature"
   ```

3. **Switch back to the main branch and merge the feature branch:**
   ```bash
   git checkout main
   git merge feature-branch
   ```

**Real-Time Example:**
Imagine you are working on a new feature for a website. You create a `feature-branch` to develop this new feature. Once the feature is complete and tested, you merge it into the `main` branch so that it becomes part of the official codebase.

**Pros of Merge:**
- Retains the complete history of commits.
- Easier to understand the development flow with a complete record of when and how branches were integrated.

**Cons of Merge:**
- Can create a complex history with many branches and merges.

---

**Git Rebase:**
Rebasing is a way to integrate changes from one branch into another by applying the commits from the source branch on top of the target branch.

**Example:**
1. **Create and switch to a new branch:**
   ```bash
   git checkout -b feature-branch
   ```

2. **Make changes and commit them:**
   ```bash
   echo "New feature" >> feature.txt
   git add feature.txt
   git commit -m "Add new feature"
   ```

3. **Rebase the feature branch onto the main branch:**
   ```bash
   git checkout main
   git pull origin main
   git checkout feature-branch
   git rebase main
   ```

4. **Resolve any conflicts that arise during rebase.**

5. **Switch back to the main branch and fast-forward:**
   ```bash
   git checkout main
   git merge feature-branch --ff-only
   ```

**Real-Time Example:**
Consider the same scenario as above. Instead of merging, you rebase the `feature-branch` onto the `main` branch. This makes the history of `main` appear as if the feature was developed in a linear sequence, making it cleaner and easier to understand.

**Pros of Rebase:**
- Creates a linear, easy-to-read project history.
- Avoids unnecessary merge commits.

**Cons of Rebase:**
- Can be complex and risky if conflicts arise.
- Rewriting history can cause issues if not done correctly, especially with shared branches.

---

#### Git Stash & Pop

**Git Stash:**
Stashing is a way to save the current state of your working directory and index without committing them. This is useful if you need to switch branches or work on something else temporarily.

**Example:**
1. **Make changes to a file:**
   ```bash
   echo "Temporary changes" >> temp.txt
   ```

2. **Stash the changes:**
   ```bash
   git stash push -m "Temporary changes to temp.txt"
   ```

3. **Switch to another branch:**
   ```bash
   git checkout another-branch
   ```

4. **Switch back to the original branch and apply the stashed changes:**
   ```bash
   git checkout main
   git stash pop
   ```

**Real-Time Example:**
You are working on a new feature but suddenly need to fix a critical bug on a different branch. You stash your changes, switch to the bug-fix branch, resolve the issue, and then return to your original branch and apply the stashed changes.

**Pros of Stash:**
- Temporarily saves work without committing.
- Allows switching branches without losing changes.

**Cons of Stash:**
- Can be easy to forget stashes, leading to confusion.

**Git Stash Pop:**
The `git stash pop` command applies the most recent stashed changes to your working directory and removes the stash from the stash list.

**Example:**
1. **Apply the stashed changes:**
   ```bash
   git stash pop
   ```

**Real-Time Example:**
After fixing the critical bug, you return to your feature branch and use `git stash pop` to restore your previous work.

**Pros of Stash Pop:**
- Quickly restore stashed changes.
- Clean up stash list by removing applied stashes.

**Cons of Stash Pop:**
- If conflicts arise, they need to be resolved manually.

### Git Branching Strategies: A Detailed Guide

Effective Git branching strategies are essential for managing your project's codebase efficiently, especially in a team environment. Below, we’ll cover common branching strategies such as `dev`, `qa`, `ppd`, `prod`, `dr`, `feature`, `bugfix`, and `hotfix` branches. We’ll also provide example commands and a textual diagram to illustrate the flow.

### Branch Types and Their Purpose

1. **Development (`dev`) Branch**:
   - The primary branch where developers integrate their code.
   - It is usually in an unstable state and continuously updated.
   - Example: `dev`

2. **Quality Assurance (`qa`) Branch**:
   - Used for testing purposes after features are integrated into the `dev` branch.
   - Example: `qa`

3. **Pre-Production (`ppd`) Branch**:
   - Used for final testing before deploying to production.
   - Example: `ppd`

4. **Production (`prod`) Branch**:
   - Contains the code that is live in production.
   - This branch should always be stable.
   - Example: `prod`

5. **Disaster Recovery (`dr`) Branch**:
   - A backup of the `prod` branch for disaster recovery purposes.
   - Example: `dr`

6. **Feature Branch**:
   - Used to develop new features for the upcoming or a distant future release.
   - Example: `feature/login`

7. **Bugfix Branch**:
   - Used to fix bugs identified in the `dev` branch.
   - Example: `bugfix/issue-123`

8. **Hotfix Branch**:
   - Used to quickly patch production code without waiting for the next release.
   - Usually branched off from `prod`.
   - Example: `hotfix/security-fix`

### Example Commands for Managing Branches

1. **Creating Branches**:
   ```sh
   # Create a development branch
   git checkout -b dev

   # Create a QA branch from dev
   git checkout -b qa dev

   # Create a pre-production branch from qa
   git checkout -b ppd qa

   # Create a production branch from ppd
   git checkout -b prod ppd

   # Create a disaster recovery branch from prod
   git checkout -b dr prod

   # Create a feature branch from dev
   git checkout -b feature/login dev

   # Create a bugfix branch from dev
   git checkout -b bugfix/issue-123 dev

   # Create a hotfix branch from prod
   git checkout -b hotfix/security-fix prod
   ```

2. **Merging Branches**:
   ```sh
   # Merge a feature branch into dev
   git checkout dev
   git merge feature/login

   # Merge a bugfix branch into dev
   git checkout dev
   git merge bugfix/issue-123

   # Merge dev into qa for testing
   git checkout qa
   git merge dev

   # Merge qa into ppd for final testing
   git checkout ppd
   git merge qa

   # Merge ppd into prod for deployment
   git checkout prod
   git merge ppd

   # Merge hotfix into prod
   git checkout prod
   git merge hotfix/security-fix

   # Merge prod into dr for backup
   git checkout dr
   git merge prod
   ```

### Real-Time Example Workflow

1. **Feature Development**:
   - Developer creates a new feature branch from `dev`.
     ```sh
     git checkout -b feature/login dev
     ```
   - Developer works on the feature and commits changes.
     ```sh
     git add .
     git commit -m "Add login feature"
     ```
   - Feature branch is merged back into `dev` after review.
     ```sh
     git checkout dev
     git merge feature/login
     ```

2. **Bug Fixing**:
   - A bug is identified and a bugfix branch is created from `dev`.
     ```sh
     git checkout -b bugfix/issue-123 dev
     ```
   - Developer fixes the bug and commits changes.
     ```sh
     git add .
     git commit -m "Fix issue 123"
     ```
   - Bugfix branch is merged back into `dev`.
     ```sh
     git checkout dev
     git merge bugfix/issue-123
     ```

3. **Testing**:
   - Code from `dev` is merged into `qa` for testing.
     ```sh
     git checkout qa
     git merge dev
     ```
   - After successful testing, `qa` is merged into `ppd` for final testing.
     ```sh
     git checkout ppd
     git merge qa
     ```

4. **Deployment**:
   - Code from `ppd` is merged into `prod` for production deployment.
     ```sh
     git checkout prod
     git merge ppd
     ```

5. **Disaster Recovery**:
   - Production code is merged into `dr` for backup.
     ```sh
     git checkout dr
     git merge prod
     ```

6. **Hotfix**:
   - A critical issue in production is fixed via a hotfix branch created from `prod`.
     ```sh
     git checkout -b hotfix/security-fix prod
     ```
   - Hotfix is applied and merged back into `prod`.
     ```sh
     git checkout prod
     git merge hotfix/security-fix
     ```

