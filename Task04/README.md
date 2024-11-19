# Git task 4

**echo "temporary changes" >> temp.txt**  
Make changes to the file without committing it.

**git status**  
Check the status of the files.

**git stash**  
To stash the changes. This command saves changes to stash and restores the working directory to the last commit state.

**git stash list**  
To view the stashed changes.

**git stash apply**  
To apply the most recent stash.

**git stash drop**  
To apply the most recent stash and drop it.

**git stash apply stash@{1}**  
To apply a specific stash.

**git stash -u**  
To stash changes including untracked files.

**git stash apply**  
To apply stashed changes including untracked files.

# Rewriting history with git rebase

**git rebase main**  
Rebase the current branch onto main. This command applies the commit from your current branch on top of the latest commit form main.

**git rebase --continue**  
Resolve any conflicts that may arise during rebase and continue.

**git rebase --abort**  
If a rebase goes wrong abort it.

## Interactive rebase (git rebase -i)

**git log --oneline**  
To view the last few commits.

**git rebase -i HEAD~3**  
Start an interactive rebase for the last three commits. This opens an editor with the list of commits in the last 3 commits.

Modify the commits by changing 'pick' to one of the following:  
**squash (combine commits)**  
**reword (edit commit message)**  
**edit (edit commit content)**  
**drop (remove commit)**

> Example of squashing two commits:  
Change the second commit from pick to squash and save.  
Git will combine the commit messages for the squashed commit.

> Complete Interactive Rebase:  
After modifying the commits, save and close the editor.  
Resolve any conflicts if prompted, then continue the rebase:  
**git rebase --continue**

# Cherry-picking commits (git cherry-pick)

**git log --oneline**  
View the commit history to find the commit hash you want to cherry-pick.

**git cherry-pick (commit-hash)**  
Cherry-pick a specific commit by its hash.  
For example: *git cherry-pick e23d8a7*

**git add .**  
**git cherry-pick --continue**  
Resolve conflicts if any, then commit the changes.

# Tagging commits (git tag)

Tag the current commit with a version number:  
**git tag -a v1.0 -m "Initial release"**

List all tags:  
**git tag**

Tag a specific commit by its hash:  
**git tag -a v1.1 (commit-hash) -m "Bug fix"**

Push a specific tag to the remote repository:  
**git push origin v1.0**

Push all the tags to the remote repository:  
**git push --tags**

# Working with remote repositories

Add a remote repository url to the project:  
**git remote add origin (repo-url)**

Fetch changes from the remote repository without merging them:  
**git fetch origin**

View fetched branches:  
**git branch -r**

Pull the latest changes from the remote repository and merge them into the local branch:  
**git pull origin main**

Push local changes to the remote repository:  
**git push origin main**

Delete a remote branch:  
**git push origin --delete feature-branch**

# Forking and contributing to open source projects

>Fork a repository on github:  
Go to a repository on GitHub and click Fork in the top right corner to create your own copy of the repository.  
Clone the forked repository to your local machine:  
**git clone https://github.com/your-username/repo.git**

Create a new branch for your changes:  
**git checkout -b fix-typo**

Make changes to the code (e.g., fix a typo in README.md), stage, and commit them:  
**git add README.md**  
**git commit -m "Fixed typo in README.md"**

Push the changes to your remote fork:  
**git push origin fix-typo**

> Create a Pull Request  
Go to your forked repository on GitHub, click on Compare & Pull Request.  
Write a description of your changes and submit the pull request to the original repository.

## Sync your fork with the original repository:

Add the original repository as a remote source:  
**git remote add upstream https://github.com/original-owner/repo.git**

Fetch changes from the original repository:  
**git fetch upstream**

Merge changes from the original repository into your local branch:  
**git checkout main**  
**git merge upstream/main**

Push the changes to your fork:  
**git push origin main**