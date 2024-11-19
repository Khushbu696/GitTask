# Git task 3

**mkdir myproject**  
**cd myproject**  
**git init**  
**git status**  
Create a folder, navigate to it, initialize it as a git repository and verify the repository status.

**git clone (repo-url)**  
Clone a remote github repository.

**cd repo**  
**ls -a**  
Verify the cloned repository stucture.

**echo "welcome to git" > file1.txt**  
**git add file1.txt**  
**git commit -m "added file1"**  
Create a file and add content to it, add the file to the staging area and save the changes with a message.

# Commit history

**git log**  
View full past commits.

**git log --oneline**  
View commit history in compact format.

**git log --oneline --graph --decorate**  
View commit history with a graphical representation.

**git log README.md**  
Filter logs for a specific file.

# Understanding Branches

**git branch**  
List all the branches.

**git branch feature-branch**  
**git checkout feature-branch**  
To create a new branch and navigate to it.

**git checkout -b feature branch**  
Create and navigate to a new branch in one step.

## Resolving merge conflicts

> Modify the same line in a file on two branches.  
**echo "main branch content" >> conflict.txt**  
**git add conflict.txt**  
**git commit -m "added conflict.txt in main branch"**

> Switch to other branch and make conflicting changes.  
**git checkout feature-branch**  
**echo "Feature branch content" > conflict.txt**  
**git add conflict.txt**  
**git commit -m "Modified conflict.txt in feature-branch"**

