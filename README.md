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


## Challenge 2: Editing Commit History

```
gymicyerekezo@icyerekezos-iMac git_advanced % git rebase -i HEAD~2
[detached HEAD 2fb8e4801da81c8c8e15d6cc3afd275fccd8f2b6] chore: Create another file
 Date: Fri Feb 28 11:33:32 2025 +0200
 1 file changed, 1 insertion(+)
Successfully rebased and updated refs/heads/main.
gymicyerekezo@icyerekezos-iMac git_advanced % 


gymicyerekezo@icyerekezos-iMac git_advanced % git log
commit fe110c2e191c7daee924470de904803429f55ce6 (HEAD -> main)
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Fri Feb 28 11:33:32 2025 +0200

    Chore: Create third and fourth files

commit 2fb8e4801da81c8c8e15d6cc3afd275fccd8f2b6
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Fri Feb 28 11:33:32 2025 +0200

    chore: Create another file
    
    Change the another file to second file

commit 021b234eae8bdca981abc41f6d966e3809cc8bb2
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Fri Feb 28 11:33:32 2025 +0200

    chore: Create initial file
```

## Challenge 3: Keeping History Tidy-Squashing Commits

```
pick 5bc10b2 chore: Create initial file
squash 172f779 chore: Create second file
pick 56cba11 chore: Create third and fourth files
pick 9df44b3 Update README.md
pick 0db89bf Update README.md
pick b2e4167 chore: Create initial file
pick 2b4d247 Chore: Create third and fourth files
pick 39e2de0 The second commit changed and the README.md updated

# Rebase 22a562e..39e2de0 onto 22a562e (8 commands)
#
# Commands:
# p, pick = use commit
# r, reword = use commit, but edit the commit message
# e, edit = use commit, but stop for amending
# s, squash = use commit, but meld into previous commit


```