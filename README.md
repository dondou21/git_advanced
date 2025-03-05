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

## Challenge 4: Splitting a commit 

```
gymicyerekezo@icyerekezos-iMac git_advanced % git reset HEAD~1
Unstaged changes after reset:
M       test2.md
gymicyerekezo@icyerekezos-iMac git_advanced % git add test3.md
gymicyerekezo@icyerekezos-iMac git_advanced % git commit -m'chore: Create third file'
On branch main
Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes not staged for commit:
        modified:   test2.md

no changes added to commit
gymicyerekezo@icyerekezos-iMac git_advanced % 
```


pick 785b42b challenge 4 done
pick 021b234 chore: Create initial file
squash 2fb8e48 chore: Create another file
pick fe110c2 Chore: Create third and fourth files


## challenge 5: Advanced Squashing
```

# Rebase 746ebef..859e61c onto 746ebef (4 commands)
#
# Commands:
# p, pick = use commit
# r, reword = use commit, but edit the commit message
# e, edit = use commit, but stop for amending
# s, squash = use commit, but meld into previous commit
# f, fixup = like "squash", but discard this commit's log message
# x, exec = run command (the rest of the line) using shell
# d, drop = remove commit
#
-- INSERT --

```

## Challlenge 6: Dropping a Commit

```
pick 172f779 chore: Create another file
pick 56cba11 chore: Create third and fourth files
pick 9df44b3 Update README.md
pick 0db89bf Update README.md
pick b2e4167 chore: Create initial file
pick 2b4d247 Chore: Create third and fourth files
pick 39e2de0 The second commit changed and the README.md updated
pick 746ebef Challenge 3 done by changing pick to squash for thr commit  Create second file
pick 785b42b challenge 4 done
pick 021b234 chore: Create initial file
pick 2fb8e48 chore: Create another file
pick fe110c2 Chore: Create third and fourth files
pick 7b762a9 the advanced squashing
drop 9d7b9ee unwanted commit message

# Rebase 5bc10b2..9d7b9ee onto 5bc10b2 (14 commands)
-- INSERT --
```



```
commit 26560b48858e9fef7631a9e27b1d3f556da92434 (HEAD -> challenge7, origin/main, origin/HEAD, main)
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Mon Mar 3 17:17:52 2025 +0200

    Challelnge 6: Dropping Commit

commit 9d7b9eee5294c1a41fc2de1573f9e0fcb2716f26
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Mon Mar 3 17:12:50 2025 +0200

    unwanted commit message

commit bc2b32911dbefdc80d8dd3784f89a862c92290c0
Merge: 859e61c 7b762a9
Author: Dondou <106757087+dondou21@users.noreply.github.com>
Date:   Mon Mar 3 17:03:04 2025 +0200

    Merge pull request #1 from dondou21/part1
    
    the advanced squashing

commit 7b762a991413102f49d02607245a84ce107e8951 (origin/part1)
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Mon Mar 3 16:47:43 2025 +0200

    the advanced squashing

commit 859e61c2d9e7f86c17a9e1b94e83e71b28341a83
Merge: 785b42b a1b01cc
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Fri Feb 28 12:32:27 2025 +0200
```