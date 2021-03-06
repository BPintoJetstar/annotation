# Saving credentials
````
git config credential.helper store
git pull
````
# Git global setup

```
git config --global user.name "Manuel Almeida"
git config --global user.email "manuel.almeida@marlo.com.au"
```
# Create a new repository

```
git clone https://gitlab.com/manuel.almeida/test.git
cd test
```

# Rename Branch
git branch -m <old_name> <new_name> 

### delete the old branch on remote - where <remote> is eg. origin
git push <remote> --delete old_name

### push the new branch to remote         
git push <remote> new_name

### Reset the upstream branch for the new_name local branch
git push <remote> -u new-name



```
cd existing_folder
git init
git remote add origin https://gitlab.com/manuel.almeida/test.git
git add .
git commit -m "Initial commit"
git push -u origin master
```

# Push to repository with branch
- Move to you working branch
- `git push -u origin <branch>`
   
   where `-u` syncronizes your local branch with the remote branch
   
# Rules to deal with branch
- If you need to update the brach use `git pull --REBASE`
- If you are done with the branch use `git merge` 

# Setting Upstream to your branch
`git push  -u origin branch`
`git push  --set-upstream repository branch`

# To save small updates without commit
- Save with git `stash <stash name>`
- Retrieve with `git stash <stash  name>`

# Return back to an old commit state 
- `git reverse -n <commit hash code>`

   Use -n param to avoid auto-commit,changes will go to stagin area but won't be commited. 
   More suitable use this on master bracn instead of `git reset` to avoid historic modification.
   If somehow you change the historic use `git push [...] --force` to bypass the error.

- `git reset<commit hash code>`

   Useful for working branches  with parameters `--soft |--hard ` to determine if you wish to keep changes or not.
   
# Resolving conflits
-  After resolving the conflicted files use `git add .` to add the files to stage.
- `git commit`continue the merge  or `git rebase --continue` if you are using rebase. 
- Finalize with `git push origing master`.
      
    Attention: DO NOT USE  `git commit -m` to solve conflicts. And ALWAYS use `--rebase` parameter when pulling from remote.
 # Remove branch
**Remote**

`git push <remote_repository> --delete <branch_name>`

**Local** 

`git branch -d <branch_name>`

  Note: The `-d` option is an alias for `--delete`, which only deletes the branch if it has already been fully merged in its upstream    branch. You could also use `-D`, which is an alias for `--delete --force`, 
   
