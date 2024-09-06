# Learn GitHub

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

6. by default initially we have "Master" name for us repo, we can change it to "main"
```
git branch -M main
```

7. Adds a new remote repository named "origin" to your local Git repository. origin is like a name for repo.
```
git remote add origin <repo name>
```

8. Push Changes to Remote Repository. "-u" meaning that future git push and git pull commands will default to this branch. "main" is branch in which you’re pushing.
```
git push -u origin main
```