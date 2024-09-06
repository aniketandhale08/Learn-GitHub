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
