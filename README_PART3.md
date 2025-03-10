# Part 3

## Challenge1: Stashing changes

```
gymicyerekezo@icyerekezos-iMac git_advanced % git add .
gymicyerekezo@icyerekezos-iMac git_advanced % git commit -m'Creation of README_PART£.md for the part 3'
[main a1c7b28] Creation of README_PART£.md for the part 3
 1 file changed, 7 insertions(+)
 create mode 100644 README_PART3.md
gymicyerekezo@icyerekezos-iMac git_advanced % git stash
No local changes to save
gymicyerekezo@icyerekezos-iMac git_advanced % git stash 
Saved working directory and index state WIP on main: a1c7b28 Creation of README_PART£.md for the part 3
gymicyerekezo@icyerekezos-iMac git_advanced % 

```

## Challenge2: Retrieviing Stashed Changes

```
gymicyerekezo@icyerekezos-iMac git_advanced % git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README_PART3.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (30de29bb41d45a37cf72701551804fea4f955c13)
gymicyerekezo@icyerekezos-iMac git_advanced % 
```
## Challenge3: Branch Merging Conflicts (Continued):

```
gymicyerekezo@icyerekezos-iMac git_advanced % git merge challenge7
Auto-merging test3.md
CONFLICT (content): Merge conflict in test3.md
Automatic merge failed; fix conflicts and then commit the result.
gymicyerekezo@icyerekezos-iMac git_advanced %  


gymicyerekezo@icyerekezos-iMac git_advanced % git status                                      
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:

        modified:   test3.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README_PART3.md

gymicyerekezo@icyerekezos-iMac git_advanced % 

```