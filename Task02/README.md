# Git task 2

**mkdir myproject**  
**cd myproject**  
**git init**  
To create a directory and initialize it as a git repository.

**echo "helo git" > file1.txt**  
**git add file1.txt**  
**git commit -m "added file1.txt"**  
To create a file, stage it and commit the file.

**echo "git is awsome" >> file1.txt**  
Make changes to the file.

**git status**  
**git diff**  
To check file status and the differences.

**git reset file1.txt**
To unstage a staged file.

**git checkout -- file1.txt**  
To discard uncommited changes.

# Branches

**git checkout -b feature-branch**  
To create a branch and switch to it.

**git branch**  
To list all the branches.

**git branch -m feature-branch feature-enhanced**  
To rename a branch from feature-branch to feature-enhanced.

> Merging branches ans handling merge conflicts  
**git checkout main**  
**git merge feature-enhanced**  
To merge the feature-enhanced branch into the main branch.

Create two conflicting branches and resolve the conflict manually.  
**git merge (branch-name)**  
Use:  
**git add (resolved file)**  
**git commit -m ""**

# Remote setup, push and pull

**git remote add origin (repo-url)**  
To add a remote repo.

**git remote -v**  
To verify the remote url.

**git push -u origin main**  
To push the changes to the remote repository.

**git pull origin main**  
To pull the changes from the remote repository.

**git clone (repo-url)**  
To clone remote repository.

# Advanced Git

**git stash**  
To stash the changes made.

**git stash apply**  
To apply the stashed changes.

**git stash drop**  
To drop the stash after applying.

**git tag -a v1.0 -m "Version 1.0 release"**  
Tag the current commit.

**git push origin v1.0**  
Push the tag to the remote repository.

Use interactive rebase to modify commit messages:  
**git rebase -i HEAD~3**  
Replace pick with edit or squash as needed.

Apply a specific commit to another branch:  
**git cherry-pick (commit-hash)**

Fork a repository and clone it locally:  
**git clone (repo-url)**

Make changes and push them:  
**git checkout -b fix-typo**  
**echo "Typo fixed" >> README.md**  
**git add README.md**  
**git commit -m "Fixed a typo"**  
**git push origin fix-typo**

Open a pull request on Github.

# Ignoring files

Create a .gitignore file:  
**echo "node_modules/" > .gitignore**  
**git add .gitignore**  
**git commit -m "added .gitignore"**

Verfiy that ignored files are not staged.  
**git status**

# Automation and Cleanup

Remove untracked files.  
**git clean -f**

Create an alias for frequently used commands:  
**git config --global alias.st status**  
**git config --global alias.cm commit**

Use the alias:  
**git st**  
**git cm -m "message"**