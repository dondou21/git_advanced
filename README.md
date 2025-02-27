# git_advanced


## Missing File Fix

```
DONDOU@DESKTOP-RJPSVMO MINGW64 ~/Desktop/git_advanced (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

DONDOU@DESKTOP-RJPSVMO MINGW64 ~/Desktop/git_advanced (main)
$ git add test4.md

DONDOU@DESKTOP-RJPSVMO MINGW64 ~/Desktop/git_advanced (main)
$ git commit --amend -m "chore: Create third and fourth files"
[main c8af1a2] chore: Create third and fourth files
 Date: Thu Feb 27 13:39:03 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

DONDOU@DESKTOP-RJPSVMO MINGW64 ~/Desktop/git_advanced (main)
$ git commit --amend -m "chore: Create third and fourth files"
[main 1babaf5] chore: Create third and fourth files
 Date: Thu Feb 27 13:39:03 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)  
 create mode 100644 test3.md
 create mode 100644 test4.md

```


