# Find changes to a file on all branches
git log --all -- git log --all -- C:\Development\localRepo\someFile.md --source

# Push all branches to a local repo
git push --all C:\Development\localRepo

# Code review 
git checkout main
git pull
git merge --no-commit --no-ff {branch}
