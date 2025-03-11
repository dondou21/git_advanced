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

## Challenge4; Resolving Merge Conflicts with a Merge Tool

```
gymicyerekezo@icyerekezos-iMac git_advanced % git mergetool --tool-help
'git mergetool --tool=<tool>' may be set to one of the following:
                opendiff
                vimdiff
                vimdiff2
                vimdiff3

The following tools are valid, but not currently available:
                araxis
                bc
                bc3
                codecompare
                deltawalker
                diffmerge
                diffuse
                ecmerge
                emerge
                examdiff
                gvimdiff
                gvimdiff2
                gvimdiff3
                kdiff3
                meld
                p4merge
                tkdiff
                tortoisemerge
                winmerge
                xxdiff

Some of the tools listed above only work in a windowed
environment. If run in a terminal-only session, they will fail.

```


## Challenge5: Understanding Detached HEAD State

```
gymicyerekezo@icyerekezos-iMac git_advanced % git checkout main 
Already on 'main'
Your branch is up to date with 'origin/main'.
gymicyerekezo@icyerekezos-iMac git_advanced % 

```
## Challenge6: Ignoring Files/Directories

```
gymicyerekezo@icyerekezos-iMac git_advanced % touch .gitignore
gymicyerekezo@icyerekezos-iMac git_advanced % /tmp
zsh: permission denied: /tmp
gymicyerekezo@icyerekezos-iMac git_advanced % /tmp
zsh: permission denied: /tmp
gymicyerekezo@icyerekezos-iMac git_advanced % cat .gitignore
/tmp%                                                                                          
gymicyerekezo@icyerekezos-iMac git_advanced % git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
gymicyerekezo@icyerekezos-iMac git_advanced % 

```