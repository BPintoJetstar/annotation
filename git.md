## Push to repository with branch
- Move to you working branch
- `git push -u origin <branch>`
   
   where `-u` syncronizes your local branch with the remote branch
   
## Rules to deal with branch
- If you need to update the brach use `git pull --REBASE`
- If you are done with the branch use `git merge` 

## Setting Upstream to your branch
`git branch --set-upstreamto=origim/[master|<other branch] <branch name>` 

## To save small updates without commit
- Save with git `stash <stash name>`
- Retrieve with `git stash <stash  name>`
## Return back to an old commit state 
- `git reverse <commit hash code>`

   More suitable use this on master bracn instead of `git reset` to avoid historic modification.
   If somehow you change the historic use `git push [...] --force` to bypass the error.

- `git resert<commit hash code>`

   Useful for working branches  with parameters `--soft |--hard ` to determine if you wish to keep changes or not.
   
   ## Resolving conflits
-  After modifiing the conflicted files use `git add .` to add the files to stage.
- `git merge --continue`continue the merge  or `git rebase --continue` if you are using rebase. 
- Finalize with `git push`.
      
    Attention: DO NOT USE  `git commit -m` to solve conflicts. And ALWAYS use `--rebase` parameter when pulling from remote.
