# Git task 1

**mkdir MyProject**  
**cd MyProject**  
To create a folder and navigate to it.

**git init**  
To initalize a git repository.

**echo "my first project" > README.md**  
To create a file and add content to it.

**git add README.md**  
To add the file to the staging area.

**git commit -m "initial commit: added README.md file"**  
To commit the file and save the changes to the staging area.

**echo "added description" >> README.md**  
To make changes to the file.

**git add README.md**  
**git commit -m "updated README.md with a description"**  
To stage and commit the changes.

**git status**  
To check the repository's current statyus.

**git log --oneline --graph --decorate**  
To view the commit history in detail.

**git clone (repsoitory url)**  
To clone a github repository in your local.

**git branch feature-login**  
To create a new branch named feature-login.  
**git checkout feature-login**  
To navigate to the branch named feature-login.  
**git checkout -b feature-login**
To create a new branch and navigate to it in one step.

**git checkout main**  
**git merge feature-login**  
To navigate to the main branch and then merge the feature-login branch to the main branch.

**git branch -m oldbranchname newbranchname**  
To rename a branch.

**git branch -d feature-login**  
To delete a branch that has been merged.

# Handling merge conflicts

> Create two branches  
**git branch branch-A**  
**git banch branch-B**

> Modify the same line in the README.md file in both branches.

> Merge branch-A into main  
**git checkout main**  
**git merge branch-A**

> Attempt to merge branch-B into main; this will create a conflict  
**git merge branch-B**

> Resolve the conflict manually by opening that README.md in your local and modify it.  
**git add README.md**  
**git commit -m "Resolved the merge conflict"**

# Advanced git operations (git stash)

**echo "temporart work" >> temp.md**  
Make changes in the file but don't commit.

**git stash**  
To stash the changes made.

**git stash list**  
To view stashed changes.

**git stash apply**  
To apply the stashed changes.

**git stash drop**  
To drop the stash after applying.

# Rewriting the history with interactive rebase

> Create multiple commits  
**echo "Commit 1" > file1.txt && git add file1.txt && git commit -m "Commit 1"**  
**echo "Commit 2" > file2.txt && git add file2.txt && git commit -m "Commit 2"**  
**echo "Commit 3" > file3.txt && git add file3.txt && git commit -m "Commit 3"**

> Squash commits into one  
**git rebase -i HEAD~3**  
Replace 'pick' with 'squash' for the second and third commits.

# Cherry-picking commits

> Create a new branch  
**git checkout -b cherry-pick-example**

> Cherry-pick a specific commit from another branch  
**git cherry-pick (commit-hash)**

# Tagging commits

**git tag -a v1.0 -m "Version 1.0 release"**  
Tag the current commit.

**git push origin v1.0**  
Push the tag to the remote repository.

# Working with remote repositories

**git remote add origin (repositry-url)**  
Add a remote repository.

**git push origin main**  
Push your changes to the remote repository.

# Forking and Contributing

> Fork a repository on GitHub.

> Clone the fork locally:  
**git clone (forked-repo-url)**

> Create a new branch, make changes, and push:  
**git checkout -b fix-typo**  
**echo "Typo fixed" >> README.md**  
**git add README.md**  
**git commit -m "Fixed a typo"**  
**git push origin fix-typo**

> Open a pull request on GitHub.