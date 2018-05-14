## Push to repository with branch
- Move to you working branch
- `git push -u origin <branch>`
   
   where `-u` syncronizes your local branch with the remote branch
   
## Rool to deal with branch
- If you need to update the brach use `git pull --REBASE`
- If you are done with the branc use `git merge` 
## Setting Upstream to your branch
`git branch --set-upstreamto=origim/[master|<other branch] <branch name>` 

## To save small updates without commit
- Save with git `stash <stash name>`
- Retrieve with `git stash <stash  name>`
