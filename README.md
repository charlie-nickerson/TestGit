# TestGit: A repo for testing github commands

## HOW TO MAKE A COMMIT IN THE PAST:
GIT_AUTHOR_DATE="2025-01-01 12:00:00" GIT_COMMITTER_DATE="2025-01-01 12:00:00" git commit -m "Going back in time"

## HOW TO UPDATE THE NAME OF A FILE IN GIT

## Automatic Method
git mv OLDNAME.md NEWNAME.md
git commit -m "Renamed OLDNAME.md to NEWNAME.md"
git push

## Manual Method
git rm OLDNAME.md
git add NEWNAME.md
git commit -m "Renamed OLDNAME.md to NEWNAME.md"
git push


## HOW TO UNDO A PUSH

## Safest Way
Step 1: Find the commit hash you want to return to:

git log

Step 2: Create a new commit that undoes the changes:

git revert <commit-hash>

Sep 3: Push the revert commit:

git push

## SUS Method
Go back one commit:

git reset --hard HEAD~1

Force push (be careful with this!):

git push --force
