# Learn Git!


Git is a type of  version manager

* To initialize a project with git
```
git init
```

* to know about the current status of git 

```
git status
```
* To add a file to the stage for committing use 

```
git add <filename>
```

* To commit a file: it means to keep record of file changes

```
git commit -m "<message>"
```

* To view git commits

```
    git log
```

* To view git commits in one line

```
    git log --oneline
```

* To add a remote repository like github

```
git remote add <name> <url>
```
example: git remote add origin https://github.com/Drisya24/learn-git.git

* To view the url of the remote repository.

```
git remote show <name>
```
Example: git remote show origin

* To push the changes to the remote repository

```
git push origin <branch>
```
But for first push of a branch use

```
git push -u origin <branch>
``` 

* If already pushed with `-u` then next time onwards use 

```
git push
```

* To create a branch

```
git branch <branch_name>
```

* To checkout/goto a branch 

```
git checkout <branch_name>
```

* To show current branch

```
git status
```
```
git branch
```


## How to resolve git conflict ?
----------------------------

Git conflict occurs when both  remote (github) and local make changes in the same file. 
Best practice to avoid conflict is to always pull the  branch & always push your branch to the remote repo.

### Solve
* if conflict occurs there will be 3 new lines which help us to distinguish between local and remote file changes. For example

```
<<<<< HEAD
<mostly your local file code>
========
<mostly the remote files>
>>>>>>>>
```
* Decide which code changes you want and keep it and delete every other lines including <<<, ==== and >>>>>>
* Then `git add <filename>`
* Then `git commit `
* press `shift + ;`
* type `wq`
* press `enter`
* Changes will be committed  in the local repo
*  Push changes to remote : `git push`
*  Done.