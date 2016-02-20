# Git

## Workflow


1. git co master
1. git pull (see if others have made changes in the meantime)
1. git co -b feature_branch
1. work work work work work work
1. git add .
1. git commit
1. git push origin feature_branch (to share your work with the team on github)

When you are done with work

1. git co master
1. git pull
1. git co feature_branch
1. git merge master (resolve merge conflicts, if any)
1. git co master
1. git merge --no-ff feature_branch
1. git push
1. git branch -d feature_branch (delete the feature branch)
