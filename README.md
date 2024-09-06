# Learn GitHub

## Create a new repository on the command line.

1. To initilize the repo on local machine.
```
git clone <repo name>
```

2. to initialize a repository.
```
git init
```

3. Create a README file.
```
touch README.md
```
you can edit readme now.

4. save the file and add it to the staging area.

```
git add README.md
```

5. Commit the changes with a message.
```
git commit -m "first commit"
```

6. By default initially we have "Master" name for us repo, we can change it to "main"
```
git branch -M main
```

7. Adds a new remote repository named "origin" to your local Git repository. origin is like a name for repo.
```
git remote add origin <repo name>
```

8. Push Changes to Remote Repository. "-u" meaning that future git push and git pull commands will default to this branch. we dont need to write "origin main" repeatedly. "main" is branch in which you’re pushing.
```
git push -u origin main
```


To make a new file in local system 
```
mkdir <file name>
```

To access it.
```
cd <file name>
```

To see the hidden files
```
git -a
```

After creating the new files in local system the got will show the "U" infront of them , whcih means they are "Untracked" files.
to check status of repo.
```
git status
```

To add this new files you can use " git add. " and then commit them.

by adding and commiting the files you are doing this all in your local system, you are not uploading them to github. to do this do commit.

if you want to add your local files to another any repo. Link your local files to remote repository on like GitHub 
```
git remote add origin <repo link>
```

Displays the URLs of the remote repositories linked to your local Git repository. used to check, the remote repository is correctly configured.
```
git remote -v
```

Used to list brances
```
git remote -v
```

## Workflow
For Local Git
```
1. Modify Files
     |
     v
2. git init      --> Initialize a local repository (if not done)
     |
     v
3. git status    --> Check the current status of changes
     |
     v
4. git add       --> Stage changes (prepare to commit)
     |
     v
5. git commit    --> Commit the changes with a message
     |
     v
6. git branch    --> (Optional) Create or switch branches
     |
     v
7. git push      --> Push to remote (if connected to one)
```

## Git Branches

1. Create a New Branch
```
git branch <branch-name>
```
2. Check how many branches we have
```
git branch
```
3. To rename the branch
```
git branch -m main
```
4. Switch to a different Branch
```
git checkout <branch-name>
```
5. To create a new branch and checkout into it simultaneously.
```
git checkout -b <branch-name>
```
6. To delete the branch. You cannot delete the branch you're currently on it. Before deleting a branch, you need to switch to a different branch.
```
git branch -d <branch-name>
```
 If you created the new branch and want to add them then, follow the same steps, "git add ." & " git commit -m"your msg" "
 and make this changes on github on that particualar branch.
 ```
 git push origin <branch name>
 ```

 ## Merging code

**Way 1**
```
git diff <branch name>         (to compare commits, branches, files & more)
```
```
git merge <branch name>        (to merge 2 branches)
```

 **Way 2**

Create PR

Pull Request: It lets you tell others about changes you've pushed to a branch in a repository on GitHub.

## Pull commands
if someone does PR to your repo and you accepted the PR on github and want to get that changes on your local system.

used to fetch and download content from a remote repo and immediately update the local repo to match that content.
```
git pull origin main
```

## Resolving the merge conflits
An event that takes place when Git is unable to automatically resolve differences in code between two commits.

if you added the code on same line where another code is alredy present then 

If you want to make same chaneges which you have did in main branch and now want to do in another branch let say "feature1"

1. Switch to the feature1 Branch
```
git checkout feature1
```
2. Merge Changes from main to feature1
```
git merge main
```
3. Resolve Any Merge Conflicts
```
git add .
```
```
git commit -m "Resolved merge conflicts from main branch"
```
4. Push the Updated feature1 Branch to GitHub
```
git push origin feature1
```
## Undoing changes

Case 1: staged changes

If you have staged changes for a specific file and want to unstage just that file, you can use
```
git reset <file name>
```
To unstage all staged changes but keep the changes in your working directory.
```
git reset
```

Case 2: commited changes (for one commit)
If you want to undo the last commit but keep the changes in your working directory.
```
git reset HEAD~1
```

Case 3: commited changes (for many commits)
If you want to undo multiple commits, there are 2 methods depending on whether you want to keep the changes or discard them.

1. Undo Multiple Commits (Keep Changes)
To undo multiple commits but keep the changes in your working directory.
```
git reset <commit-hash>
```
2. Undo Multiple Commits (Discard Changes)
To undo multiple commits and discard all changes. this will reflets undo in local system
```
git reset --hard <commit-hash>
```

Find the Commit Hash
```
git log
```