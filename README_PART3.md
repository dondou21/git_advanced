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

## Challenge7: Working with Tags
```
gymicyerekezo@icyerekezos-iMac git_advanced % git tag v1.0
gymicyerekezo@icyerekezos-iMac git_advanced % 

```

## Challenge8: Listing and Deleting Tags

```
gymicyerekezo@icyerekezos-iMac git_advanced % git tag        
v1.0
gymicyerekezo@icyerekezos-iMac git_advanced % git tag -d v1.0
Deleted tag 'v1.0' (was 304e0c6)
gymicyerekezo@icyerekezos-iMac git_advanced % git tag        
gymicyerekezo@icyerekezos-iMac git_advanced % 

```

## Challenge9: Pushing Local Work into Remote Repositories
```
gymicyerekezo@icyerekezos-iMac git_advanced % git add .
gymicyerekezo@icyerekezos-iMac git_advanced % git commit -m 'Challenge 8 done '
[main b0dc0f5] Challenge 8 done
 1 file changed, 12 insertions(+)
gymicyerekezo@icyerekezos-iMac git_advanced % git push 
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 403 bytes | 403.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/dondou21/git_advanced.git
   2b7fc21..b0dc0f5  main -> main
gymicyerekezo@icyerekezos-iMac git_advanced %

```
## Challenge10: Pulling Changes form Remote Repositories
```
gymicyerekezo@icyerekezos-iMac git_advanced % git pull origin main 
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), done.
From https://github.com/dondou21/git_advanced
 * branch            main       -> FETCH_HEAD
   b0dc0f5..9c180fe  main       -> origin/main
Updating b0dc0f5..9c180fe
Fast-forward
 README_PART3.md | 21 ++++++++++++++++++++-
 1 file changed, 20 insertions(+), 1 deletion(-)
gymicyerekezo@icyerekezos-iMac git_advanced % 

```