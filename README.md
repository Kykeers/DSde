# Домашнее задание #3

| command  | description | 
|----------|----------------------|
|**local git**
| git init | intialise local repo 
| git add *filename* | add *filename* for future commit 
| git commit -m *message* | save current changes in added files with attached *message*
| git log | show list of changes during this work
| **branches**
| git branch *branchname* | create a new branch
| git checkout *branchname* | switch to another branch
| git merge *branchname* | import all changed from *branchname* into current branch and prepare for conflict resolving
| git branch -d *branchname* | delete *branchname*
| git branch -D *branchname* | delete *branchname* even with unmerged changes
| **github and the power of Internet**
| git remote add origin *link* | create a link between local and remote repo 
| git push -u origin main | first push of local commits to remote repo
| git push | every other push
| git pull | update local repo with changes in remote repo
| git clone *link* | also create a link
| git push | also can be used to get info from the terminal regarding correct way of pushing