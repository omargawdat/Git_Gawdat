![image](https://github.com/omargawdat/Git_Gawdat/assets/53629777/a0ba577e-e897-4008-babf-abb8fbb446dd)



# Table of Contents

- [Git Commands [Setup]](#git-commands-setup)
  - [Git Init](#git-init)
  - [Git Clone](#git-clone)

- [Git Commands [Files Management]](#git-commands-files-management)
  - [Git Add](#git-add)
  - [Git rm](#git-rm)
  - [Git restore](#git-restore)
  - [Git stash](#git-stash)

- [Git Commands [Branch & Merging]](#git-commands-branch-merging)
  - [Git commit](#git-commit)
  - [Git reset](#git-reset)
  - [Git revert](#git-revert)
  - [Git cherry-pick](#git-cherry-pick)
  - [Git branch](#git-branch)
  - [Git merge](#git-merge)
  - [Git rebase](#git-rebase)
  - [Git switch](#git-switch)

- [Git Commands [Synchronization]](#git-commands-synchronization)
  - [Git remote](#git-remote)
  - [Git push](#git-push)
  - [Git fetch](#git-fetch)
  - [Git pull](#git-pull)

- [Git Commands [History]](#git-commands-history)
  - [Git checkout](#git-checkout)
  - [Git status](#git-status)
  - [Git diff](#git-diff)
  - [Git log](#git-log)
  - [Git show](#git-show)
  - [Git bisect](#git-bisect)
  - [Git reflog](#git-reflog)

---

# Git Commands [Setup]

## Git Init

**Purpose:**
The `git init` command is used to create a new `.git` directory to track the history of the project.

**Example Usage:**

- To initialize a new Git repository in the current directory, you can simply use:

    ```bash
    git init
    
    ```

- To create a new Git repository in a specific directory:

    ```bash
    git init my_project_path
    ```
---

## Git Clone

**Purpose:**

The **`git clone`** command is used to create a copy of an existing Git repository into a new directory on your local
machine.

**Example Usage:**

- To clone a repository into a directory named after the repository itself:

    ```bash
    git clone https://github.com/example/repo.git
    ```

# Git Commands [Files management]

## Git Add

**Purpose:**

The `git add` command is used to stage changes in your working directory for the next commit.

**Usage:**

- **Add Specific Files:**

    ```bash
    git add file.txt
    
    ```

  This stages 'file.txt' for the next commit.

- **Add All Changes in the Directory:**

    ```bash
    git add .
    
    ```

  This stages all changes in the current directory for the next commit.
---

## Git rm

### **Purpose:**

The `git rm` command is used to remove files from your working directory and staging area.

### **Usage:**

- **Remove and Delete File:**

    ```bash
    git rm file.txt
    
    ```

  This command removes 'file.txt' from both the staging area and the working directory.

- **Remove from Staging Only:**

    ```bash
    git rm --cached file.txt
    
    ```

  This removes 'file.txt' from staging but does not delete it from the working directory.
---

## Git restore

**Purpose:**

The `git restore` command is used to discard changes in your working directory, restoring files to their last committed
state. This is particularly useful for quickly undoing changes without altering the commit history.

### Usage:

1. **Restore a File to the Last Commit:**
    - **Command:**

        ```bash
        git restore index.html
        ```

    - **Explanation:** This command discards any local modifications to the specified file and restores it to the state
      of the last commit. It's a quick way to revert changes to a file that you do not wish to keep.
2. **Restore a File from a Specific Commit:**
    - **Command:**

        ```bash
        git restore --source=a1b2c3d4 index.html
        ```

    - **Explanation:** Allows you to restore a file to the state it was in at a specific commit. This is useful when you
      need to revert a file back to a particular version from your commit history.
3. **Restore All Files to the Last Commit:**
    - **Command:**

        ```bash
        git restore .
        
        ```

    - **Explanation:** This command discards any local modifications to all files in the working directory, restoring
      them to the state of the last commit. It's a convenient way to undo all changes in your working directory at once.

Sure, here are the Git commands listed in the image with "##" before each one:
---

## Git stash

**Purpose:**

The `git stash` command temporarily shelves (stashes) changes you've made to your working directory so you can work on
something else, then come back and re-apply them later on. This is particularly useful for managing work in progress
that is not ready to commit, allowing you to switch contexts quickly and maintain a clean working directory.

### Usage:

1. **Stash Current Changes:**
    - **Command:**

        ```bash
        git stash
        ```

    - **Explanation:** This command stashes the changes in your working directory and index. It saves your modifications
      and staged changes temporarily to a stack of unfinished changes that you can reapply at any time.
2. **List Stashed Entries:**
    - **Command:**

        ```bash
        git stash list
        ```

    - **Explanation:** Displays a list of all stashed changes available in your repository. Each entry is stored in a
      stack and can be applied or removed as needed.
3. **Apply the Latest Stashed Entry:**
    - **Command:**

        ```bash
        git stash apply
        ```

    - **Explanation:** This command re-applies the most recently stashed changes to your current working directory
      without deleting the stash.
4. **Drop a Stash Entry:**
    - **Command:**

        ```bash
        git stash drop stash@{0}
        ```

    - **Explanation:** Removes a specific stash entry from the list of stashed changes. `stash@{0}` refers to the latest
      stash.
5. **Pop the Latest Stash:**
    - **Command:**

        ```bash
        git stash pop
        ```

    - **Explanation:** This command applies the most recent stashed changes and then removes them from the stash list.
      It combines `apply` and `drop` in one step, making it a quick way to continue working on stashed changes.
6. **Clear all the Stashes:**
    - **Command:**

        ```bash
        git stash clear
        ```

    - **Explanation:** This command delete all the stashes.

# Git Commands [Branch & Merging]

## Git commit

### **Purpose:**

The `git commit` command captures a snapshot of your project's currently staged changes, saving them to your local
repository as a new commit.
![image](https://github.com/omargawdat/Git_Gawdat/assets/53629777/41d0dc01-fbca-4d1d-8c91-1023a4c1b15e)



### **Usage:**

- **Standard Commit with Message:**

    ```bash
    git commit -am "Your detailed commit message"
    
    ```

  stages and commits changes in all tracked files, skipping the manual staging step.

- **Amend a Commit:**

    ```bash
    git commit --amend -m "New commit message"
    
    ```

  remove the last commit and replace it with a new commit with the updated changes, noting that this changes the hash of
  the commit.


### Git Commands [Branch & Merging]

#### Git commit

**Purpose:**

The `git commit` command captures a snapshot of your project's currently staged changes, saving them to your local repository as a new commit.

**Usage:**

- **Standard Commit with Message:**

    ```bash
    git commit -am "Your detailed commit message"
    ```

  Stages and commits changes in all tracked files, skipping the manual staging step.

- **Amend a Commit:**

    ```bash
    git commit --amend -m "New commit message"
    ```

  Removes the last commit and replaces it with a new commit with the updated changes, noting that this changes the hash of the commit.

**Commit Message Naming Conventions:**

- **feat:** A new feature for the user, not a new feature for build scripts.
  - Example: `git commit -m "feat: add user login functionality"`

- **fix:** A bug fix for the user, not a fix to a build script.
  - Example: `git commit -m "fix: resolve issue with user authentication"`

- **chore:** Changes to the build process or auxiliary tools and libraries such as documentation generation.
  - Example: `git commit -m "chore: update dependencies"`

- **docs:** Documentation only changes.
  - Example: `git commit -m "docs: update README with installation instructions"`

- **style:** Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc.).
  - Example: `git commit -m "style: format code according to style guidelines"`

- **refactor:** A code change that neither fixes a bug nor adds a feature.
  - Example: `git commit -m "refactor: reorganize code for better readability"`

- **perf:** A code change that improves performance.
  - Example: `git commit -m "perf: optimize database queries"`

- **test:** Adding missing tests or correcting existing tests.
  - Example: `git commit -m "test: add unit tests for user service"`

- **ci:** Changes to our CI configuration files and scripts.
  - Example: `git commit -m "ci: update Travis CI configuration"`

---

## Git reset

**Purpose:**

The `git reset` command is used to undo changes in your Git repository, allowing you to reset the HEAD, staging area,
and working directory to a previous state. This command can be very powerful and is typically used to correct mistakes,
clean up commits, or alter the history of a branch, noting that  `git reset` moves both the branch and the head into a
specific commit.

| Aspect            | git reset --soft                          | git reset --mixed                    | git reset --hard                            |
|-------------------|-------------------------------------------|--------------------------------------|---------------------------------------------|
| Staging Area      | Unchanged                                 | Resets to match the specified commit | Resets to match the specified commit        |
| Working Directory | Unchanged                                 | Unchanged                            | Resets to match the specified commit        |
| Usage             | Undo commits while keeping changes staged | Undo commits and unstage changes     | Completely undo commits and discard changes |

### Usage:

1. **Git Reset --soft:**
    - **Command:**

        ```bash
        git reset --soft <commit-hash>
        
        ```

    - **Explanation:** Moves the HEAD to the specified commit but leaves your staging area and working directory
      unchanged. This is useful if you want to redo your last commit differently.
2. **Git Reset --mixed (Default):**
    - **Command:**

        ```bash
        git reset --mixed <commit-hash>
        
        ```

    - **Explanation:** Resets the HEAD to the specified commit and also resets the staging area, but keeps your working
      directory unchanged. This is the default mode when no option is specified.
3. **Git Reset --hard:**
    - **Command:**

        ```bash
        git reset --hard <commit-hash>
        
        ```

    - **Explanation:** This is the most thorough reset, as it resets the HEAD, staging area, and working directory to
      match a specific commit. Use this with caution, as it discards all changes in the staging area and working
      directory.
---

## Git revert

**Purpose:**

The `git revert` command is used to undo changes made by a previous commit in your project's history by creating a new
commit that reverses the effects of the targeted commit. This command is particularly valuable in shared repositories
because it preserves the overall project history, rather than removing or rewriting commits that others may have based
their work on.

<img width="475" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/7d9c2992-75f7-4bed-98ec-d55c8f0bf7d4">


### Usage:

1. **Revert a Single Commit:**
    - **Command:**

    ```bash
    git revert <commit-hash>
    
    ```

    - **Explanation:** This command creates a new commit that reverses the changes introduced by the specified commit.
      The original commit remains in the history, ensuring that the overall project history is preserved. For example,
      if you revert commit `C`, a new commit `C'` is created that undoes the changes made by `C`.
2. **Revert a Range of Commits:**
    - **Command:**

    ```bash
    git revert <oldest-commit-hash>^..<newest-commit-hash>
    
    ```

    - **Explanation:** This command reverts a sequence of commits from the specified range. Each commit in the range is
      reverted in reverse order, creating new commits that undo the changes of the original commits. For example, if you
      revert commits from `D` to `F`, new commits `F'`, `E'`, and `D'` are created to undo the changes introduced by
      commits `D`, `E`, and `F`.
---

## Git cherry-pick

**Purpose:**

The `git cherry-pick` command is used to selectively apply changes from specific commits from another branch into your
current branch. This tool is particularly useful for incorporating precise changes without the need to merge an entire
branch's history.

<img width="497" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/81becb81-cd77-44ea-ac68-801d1a5508e9">

### Core Usage

1. **Cherry-pick a Single Commit:**
    - **Command:**

    ```bash
    git cherry-pick <commit-hash>
    
    ```

    - **Explanation:** This command applies the changes from the specified commit into your current branch.
2. **Cherry-pick Multiple Commits:**
    - **Command:**

    ```bash
    git cherry-pick <start-commit-hash>^..<end-commit-hash>
    
    ```

    - **Explanation:** This command applies a range of commits from the specified start commit to the end commit into
      your current branch. The caret symbol (`^`) ensures all specified commits are included.
3. **Cherry-pick with Conflict Resolution:**
    - **Command:**

    ```bash
    git cherry-pick --continue
    
    ```

    - **Explanation:** If a conflict occurs during cherry-picking, this command continues the cherry-pick process after
      conflicts have been manually resolved. This approach allows you to address conflicts that arise, ensuring changes
      are applied correctly.
---

## Git tag

**Purpose:**

The `git tag` command is used to create references to specific points in Git history. Tags are often used to mark
releases (e.g., v1.0, v2.0) and are similar to branches, but unlike branches, tags are immutable pointers to commits.

<img width="750" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/6d08203e-c477-4748-84f3-c1f14f96f23d">

### Usage:

1. **Create a Lightweight Tag:**
    - **Command:**

        ```bash
        git tag <tag-name>
        git tag v1.0
        
        ```

    - **Explanation:** This creates a lightweight tag, which is simply a name that points to a specific commit. It does
      not store any extra metadata beyond the commit it points to.
2. **Create an Annotated Tag:**
    - **Command:**

        ```bash
        git tag -a <tag-name> -m "Tag message"
        git tag -a v1.0 -m "Initial release"
        
        ```

    - **Explanation:** Annotated tags store additional information, such as the tagger's name, email, date, and a
      message. This is useful for providing more context about the tag.
3. **View Tags:**
    - **Command:**

        ```bash
        git tag
        
        ```

    - **Explanation:** Lists all tags in the repository. Annotated and lightweight tags are both displayed.
4. **Delete a Tag:**
    - **Command:**

        ```bash
        git tag -d <tag-name>
        git tag -d v1.0
        
        ```

    - **Explanation:** Deletes a tag from the local repository. This does not affect the commits or branches, only the
      tag itself.

## Git branch

**Purpose:**

The `git branch` command is used to create, list, rename, and delete branches in your Git repository. Branches are
essential for managing different lines of development, allowing you to work on multiple features or fixes
simultaneously.

### Usage:

1. **List All Branches:**
    - **Command:**

        ```bash
        git branch
        ```

    - **Explanation:** Lists all branches in the repository.
2. **Rename a Branch:**
    - **Command:**

        ```bash
        git branch -m <old-branch-name> <new-branch-name>
        git branch -m feature-branch new-feature-branch
        ```

    - **Explanation:** Renames an existing branch from `<old-branch-name>` to `<new-branch-name>`. If you omit the old
      branch name, it renames the current branch.
3. **Delete a Branch:**
    - **Command:**

        ```bash
        git branch -d <branch-name>
        git branch -d feature-branch
        ```

    - **Explanation:** Deletes the specified branch. This is a safe operation that Git will prevent if the branch has
      unmerged changes. To force delete, use `D`.

## Git merge

**Purpose:**

The `git merge` command is used to integrate changes from one branch into another. This fundamental Git operation
combines separate development histories. Depending on the situation, merging can result in a fast-forward merge, a merge
commit, or may require conflict resolution when changes overlap in conflicting ways.

### Usage:

1. **Merge Another Branch into Your Current Branch:**

- **Command:**

    ```bash
    git merge feature_branch
    ```

    - **Fast Forward Merge**
        - use the tag `--ff` to avoid Fast Forward

        <img width="253" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/7e44d370-9493-4dc8-8cff-10fcb57e9841">

    - **Recursive Merge**  three-way merge):

        <img width="256" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/bec558d6-58de-48e2-afcc-a43053959c9c">

1. **Abort a Merge in Case of Conflict:**
    - **Command:**

        ```bash
        git merge --abort
        
        ```

    - **Explanation:** This command aborts the merge process and returns your project to the state before the merge
      began, effectively undoing the merge attempt and leaving `main` at commit `C` and `feature_branch` at commit `E`.
2. **Squash Merge:**
    - **Command:**

    ```bash
    git merge --squash feature_branch
    ```

    - **Explanation:** This type of merge condenses all the changes from the source branch into a single commit on the
      target branch. The history of the source branch is not preserved, and the changes is just staged without actual
      committing them.
      
      <img width="404" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/edd42cc1-0d19-4e62-be0c-667929b202a2">

---

## Git rebase

### **Purpose:**

The `git rebase` command is used to move or combine a sequence of commits to a new base commit. It's a powerful
alternative to merging that can help maintain a cleaner, more linear project history. Rebasing rewrites the commit
history by applying changes from one branch onto another, which can simplify the merging process.

<img width="504" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/f81f8b6b-66f2-4158-9b07-e4f5d304a577">


### Warning:

- **Handle With Care:** Rebase commits that are local to your repository and have not been shared with others to avoid
  complications in the shared project history.

### Usage:

1. **Rebase the Current Branch onto Another Branch:**
    - **Command:**

        ```bash
        git rebase main
        
        ```

    - **Explanation:** This command takes all the changes that were made in the current branch since it diverged
      from `main` and reapplies them on top of the latest commit on `main`. The result is a cleaner, linear history.
2. **Interactive Rebase:**
    - **Command:**

        ```bash
        git rebase -i <commit-hash>
        
        ```

    - **Explanation:** Interactive rebase allows you to modify commits as you reapply them. You can reorder, remove, or
      alter commits in the process. It's particularly useful for cleaning up your commit history before merging a
      feature branch.
3. **Handling Conflicts During Rebase:**
    - **Scenario:**
        - **Attempt Rebase:**

            ```bash
            git rebase main
            
            ```

        - **During Rebase with Conflicts:** If conflicting changes are detected, Git will pause the rebase and mark the
          files as conflicted.
        - **Resolve Conflicts and Continue:**

            ```bash
            git add <resolved-files>
            git rebase --continue
            
            ```

        - **Abort Rebase if Needed:**

            ```bash
            git rebase --abort
            
            ```

        - **Explanation:** If conflicts arise, you need to resolve them manually and continue the rebase. If the rebase
          needs to be aborted, you can use the `-abort` option to return the branch to its original state before the
          rebase began.
---

## Git switch

**Purpose:**

The `git switch` command is designed to change branches more safely and straightforwardly than the older `git checkout`
method. It helps you switch between existing branches or create and switch to new ones.

### Usage:

1. **Switch to an Existing Branch:**
    - **Command:**

        ```bash
        git switch <branch-name>
        git switch feature-branch
        ```

    - **Explanation:** This command switches your current working directory to the specified branch, updating both the
      working directory and the `HEAD` to point to the chosen branch.
2. **Create and Switch to a New Branch:**
    - **Command:**

        ```bash
        git switch -c new-feature
        ```

    - **Explanation:** This command creates a new branch named `<new-branch-name>` and immediately switches to it. This
      is a quick way to start working on a new feature without affecting the current branch.
3. **Switch to the Previous Branch:**
    - **Command:**

        ```bash
        git switch -
        ```

    - **Explanation:** This command switches back to the previous branch you were working on. It's a handy shortcut for
      toggling between two branches.

# Git Commands [Synchronization]

## Git remote

**Purpose:**

The `git remote` command is used to manage a set of tracked repositories. It allows you to view, add, and remove remote
repositories that are associated with your local repository.

**Usage:**

1. **Listing All Remotes:**

    ```bash
    git remote -v
    ```

2. **Adding a Remote Repository:**

    ```bash
    git remote add origin <https://github.com/user/repo.git>
    
    ```

3. **Removing a Remote Repository:**

    ```bash
    git remote remove origin
    
    ```

4. **Renaming a Remote Repository:**

    ```bash
    git remote rename origin upstream
    
    ```

5. **Showing Details of a Specific Remote:**

    ```bash
    git remote show origin
    
    ```

## Git push

**Purpose:**

The `git push` command is used to upload local repository content to a remote repository. Pushing is how you transfer
commits from your local repository to a remote repository, sharing your changes with others and integrating them into
the shared project.

### Usage:

1. **Push to a Remote Repository:**
    - **Command:**

        ```bash
        git push origin main
        ```

    - **Explanation:** This command pushes the specified branch to the specified remote repository. The `remote` is
      typically `origin`, and the `branch-name` is the branch you want to push. This transfers all commits from the
      local branch to the remote branch.
2. **Push All Branches:**
    - **Command:**

        ```bash
        git push --all origin
        ```

    - **Explanation:** This pushes all local branches to the specified remote repository. It ensures that every branch
      is up-to-date on the remote.
3. **Push Tags:**
    - **Command:**

        ```bash
        git push origin v1.0
        ```

    - **Push All Tags:**

        ```bash
        git push --tags
        ```

    - **Explanation:** These commands push tags to the remote repository. Tags are often used to mark releases, so
      pushing them ensures that all collaborators can see and use the same reference points.
4. **Force Push:**
    - **Command:**

        ```bash
        git push origin main --force
        ```

    - **Explanation:** Force pushing overwrites the remote branch with your local branch, discarding any conflicting
      changes on the remote. This can be useful in certain situations but should be used with caution as it can
      overwrite others' work.
5. **Set Upstream for a Branch:**
    - **Command:**

        ```bash
        git push --set-upstream origin feature-branch
        ```

    - **Explanation:** This sets the remote branch as the upstream for the local branch, making future pushes simpler.
      After setting the upstream, you can push using just `git push`.
---

## Git fetch

**Purpose:**

The `git fetch` command is used to download commits, files, and refs from a remote repository into your local
repository. Unlike `git pull`, `git fetch` does not automatically merge the changes into your working branch. Instead,
it updates your remote-tracking branches, allowing you to review changes before integrating them.

<img width="768" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/fdf07c9b-2295-4d7d-902a-a9d7aa599a0c">

### Usage:

1. **Fetch Changes from a Remote Repository:**
    - **Command:**

        ```bash
        git fetch <remote>
        git fetch origin
        ```

    - **Explanation:** This command downloads all the changes from the specified remote repository (`origin` is the
      default remote name) but does not merge them into your local branches. The changes are available in your
      remote-tracking branches (e.g., `origin/main`).
2. **Fetch a Specific Branch:**
    - **Command:**

        ```bash
        git fetch <remote> <branch-name>
        git fetch origin main
        ```

    - **Explanation:** Fetches only the specified branch from the remote repository. This can be useful if you are only
      interested in updates from a particular branch.
3. **Fetch All Remotes:**
    - **Command:**

        ```bash
        git fetch --all
        ```

    - **Explanation:** Fetches changes from all configured remotes. This ensures that all your remote-tracking branches
      are up-to-date with their respective remote repositories.

### Important Notes:

- **Safe Operation:** `git fetch` is a safe operation as it only updates your remote-tracking branches and does not
  affect your working directory or local branches. This allows you to review changes before deciding to merge them.
- **Review Before Integrating:** After fetching, you can review the changes in your remote-tracking branches
  using `git log`, `git diff`, or other commands before integrating them into your local branches with `git merge`
  or `git rebase`.
---

## Git pull

**Purpose:**

The `git pull` command is used to fetch and integrate changes from a remote repository into the current branch of your
local repository. This command combines `git fetch` (which downloads changes from a remote repository) and `git merge` (
which integrates those changes into your local branch).

<img width="770" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/4a403cb2-0654-4f36-9906-94bf0165f970">

### Usage:

1. **Pull Changes from a Remote Repository:**
    - **Command:**

        ```bash
        git pull origin main
        ```

    - **Explanation:** This command fetches the changes from the specified branch on the specified remote (`origin` is
      the default remote name) and merges them into the current branch of your local repository.
2. **Pull with Rebase:**
    - **Command:**

        ```bash
        git pull --rebase origin main
        ```

      <img width="716" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/c87cabaf-551d-4d27-88e4-009dd7aaab99">


    - **Explanation:** This command fetches changes from the remote branch and then rebases your local commits on top of
      the fetched commits, rather than merging them. This can result in a cleaner project history by avoiding merge
      commits.
3. **Pull All Remote Changes:**
    - **Command:**

        ```bash
        git pull --all
        
        ```

    - **Explanation:** This fetches and merges changes from all branches in the remote repository into their
      corresponding local branches.
    <img width="746" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/21da1564-b680-48a4-989d-98c7db4fb436">

# Git Commands [History]

## Git checkout

**Purpose:**

The `git checkout` command is used to switch between branches or restore working tree files. A key usage is to check out
a specific commit, putting your repository in a "detached HEAD" state. In this state, the HEAD refers directly to a
commit instead of a branch. This is useful for reviewing history, but it's important to note that commits made in a
detached HEAD state are at risk of being lost if not properly tracked or merged into a branch.

### Usage:

1. **Checkout a Specific Commit:**
    - **Command:**

        ```bash
        git checkout a1b2c3d4
        ```

    - **Explanation:** This command switches the HEAD to point directly at the specified commit, rather than a branch.
      It allows you to navigate and explore the historical state of your code at that specific commit.
2. **Checkout a Tag:**
    - **Command:**

        ```bash
        git checkout <tag-name>
        git checkout v1.0
        ```

    - **Explanation:** Checks out the commit associated with the tag, placing the repository in a "detached HEAD" state.
      This means you are not on any branch, just viewing the state of the repository at the tagged commit.
---

## Git status

**Purpose:**

The `git status` command is used to display the state of the working directory and the staging area. It shows which
changes have been staged, which have not, and which files are not being tracked by Git. This command helps you
understand the current status of your project.

### Usage:

1. **View the Status of Your Repository:**
    - **Command:**

        ```bash
        git status
        
        ```

### Output Explanation:

1. **Untracked Files:**
    - **Output Example:**

        ```
        Untracked files:
          (use "git add <file>..." to include in what will be committed)
            newfile.txt
        
        ```

    - **Explanation:** These are files that are new to the repository and have not yet been added to Git's tracking
      system. Use `git add <file>` to start tracking them.
2. **Changes Not Staged for Commit:**
    - **Output Example:**

        ```
        Changes not staged for commit:
          (use "git add <file>..." to update what will be committed)
          (use "git restore <file>..." to discard changes in working directory)
            modified:   file1.txt
            deleted:    file2.txt
        
        ```

    - **Explanation:** These files have been modified or deleted but are not yet staged for commit. Use `git add <file>`
      to stage the changes or `git restore <file>` to discard them.
3. **Changes to Be Committed:**
    - **Output Example:**

        ```
        Changes to be committed:
          (use "git restore --staged <file>..." to unstage)
            new file:   newfile.txt
            modified:   file3.txt
        
        ```

    - **Explanation:** These files have been staged and are ready to be committed. Use `git commit` to save these
      changes to the repository, or `git restore --staged <file>` to unstage them if you need to make further changes.
---

## Git diff

**Purpose:**

The `git diff` command is used to show the differences between various Git data sources, such as the working directory,
staging area, and commits. It allows you to see what changes have been made before committing them, helping you review
and manage changes effectively.

### Usage:

1. **View Changes Between a Commit and the Working Directory:**
    - **Command:**

        ```bash
        git diff <commit-hash>
        git diff a1b2c3d4
        
        ```

    - **Explanation:** This command shows the differences between a specific commit and the current state of the working
      directory. It helps you see what has changed since that commit.
2. **View Changes Between Commits:**
    - **Command:**

        ```bash
        git diff <commit-hash1> <commit-hash2>
        git diff a1b2c3d4 e5f6g7h8
        
        ```

    - **Explanation:** This command shows the differences between two specific commits. It allows you to compare the
      changes introduced by different commits.
---

## Git log

**Purpose:**

The `git log` command is used to display the commit history of a repository. It shows a list of commits, starting with
the most recent and going back in time, along with details about each commit, such as the author, date, and commit
message. This command is essential for tracking changes, understanding the history of a project, and identifying
specific commits.

### Usage:

1. **View Commit History:**
    - **Command:**

        ```bash
        git log
        ```

    - **Explanation:** This command displays the full commit history of the current branch, showing details about each
      commit in reverse chronological order.
2. **View a Specific Number of Commits:**
    - **Command:**

        ```bash
        git log -n 5
        ```

    - **Explanation:** This command limits the output to the specified number of most recent commits. For
      example, `git log -n 5` shows the last 5 commits.
3. **View Commit History for a Specific File:**
    - **Command:**

        ```bash
        git log index.html
        ```

    - **Explanation:** This command shows the commit history for a specific file, allowing you to see changes made to
      that file over time.
4. **View Commit History with Graph:**
    - **Command:**

        ```bash
        git log --oneline --graph --decorate --all
        ```

    - **Explanation:** This command adds a graphical representation of the branch structure to the commit history,
      showing the commit hash and message in a compact format.

      ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/2225daf2-69fb-4fd3-916e-42f5968f89c9/e20f3651-fc00-4fff-835e-ef95b1cb4813/Untitled.png)
---

## Git show

**Purpose:**

The `git show` command is used to display detailed information about various Git objects, such as commits, tags, and
file changes. It provides a comprehensive view of the changes introduced by a specific commit, including the commit
message, author, date, and the actual changes made to the files.

### Usage:

1. **Show Details of a Specific Commit:**
    - **Command:**

        ```bash
        git show <commit-hash>
        git show a1b2c3d4
        ```

    - **Explanation:** This command displays detailed information about the specified commit, including the commit
      message, author, date, and the diff of changes introduced by that commit.
2. **Show Changes for a Specific File in a Commit:**
    - **Command:**

        ```bash
        git show <commit-hash>:<file-name>
        git show a1b2c3d4:index.html
        ```

    - **Explanation:** This command shows the changes made to a specific file in the specified commit. It helps you
      understand what changes were made to that particular file.
3. **Show Details of a Tag:**
    - **Command:**

        ```bash
        git show <tag-name>
        git show v1.0
        ```

    - **Explanation:** This command displays detailed information about the specified tag, including the tag message and
      the commit it points to. Annotated tags will show the additional metadata stored with the tag.
---

## Git bisect

**Purpose:**

The `git bisect` command is used to perform a binary search through your commit history to find the specific commit that
introduced a bug or issue. This command is incredibly powerful for isolating when a problem was introduced in a
codebase, significantly speeding up the debugging process.

<img width="674" alt="image" src="https://github.com/omargawdat/Git_Gawdat/assets/53629777/30b7db34-d5c8-40b1-876d-9ffc050d9cfb">

### Usage:

1. **Start Bisecting:**
    - **Command:**

        ```bash
        git bisect start
        ```

    - **Explanation:** This command initiates the bisect process. It prepares Git to start the binary search through the
      commit history.
2. **Mark the Current Commit as Bad:**
    - **Command:**

        ```bash
        git bisect bad
        ```

    - **Explanation:** Marks the current commit as a "bad" commit, indicating that it contains the bug or issue.
3. **Mark a Known Good Commit:**
    - **Command:**

        ```bash
        git bisect good a1b2c3d4
        ```

    - **Explanation:** Marks a specific commit as "good," indicating that the bug or issue was not present at this point
      in the history. This commit should be before the introduction of the bug.
4. **Perform the Bisect Process:**
    - **Explanation:** After marking the good and bad commits, Git will automatically check out the midpoint commit
      between the good and bad commits. You need to test this commit:
        - If the commit is bad:

            ```bash
            git bisect bad
            ```

        - If the commit is good:

            ```bash
            git bisect good
            ```

    - Git will continue this process, each time halving the number of commits to test, until it isolates the exact
      commit that introduced the bug.
5. **Finish the Bisect Process:**
    - **Command:**

        ```bash
        git bisect reset
        ```

    - **Explanation:** Once the problematic commit is found, this command ends the bisect process and resets the
      repository to the state it was in before `git bisect` started.
---

## Git reflog

### Git Reflog Command Overview

**Purpose:**

The `git reflog` command is used to view the reference log, which records updates to the tip of branches and other
references in your Git repository. It provides a history of all the changes made to the references (e.g., branch heads,
tags) in your repository, including actions like commits, resets, checkouts, and merges. This command is particularly
useful for recovering lost commits and understanding the history of changes to your branches.

### Usage:

1. **View the Reference Log:**
    - **Command:**

        ```bash
        git reflog
        ```

        ```
        git reset --hard HEAD@{2}
        ```

    - **Explanation:** This command displays the reference log for the current branch. It shows a list of all changes
      made to the branch head, including the commit hash, action taken, and a brief description.
2. **View the Reference Log for a Specific Branch:**
    - **Command:**

        ```bash
        git reflog show <branch-name>
        git reflog show main
        
        ```

    - **Explanation:** This command shows the reference log for the specified branch. It is useful for tracking changes
      to branches other than the current one.
