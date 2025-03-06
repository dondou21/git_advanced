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

## Challenge 7: Reordering Commits

### Before Reordering
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
### After Reordering

```

Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Wed Mar 5 10:47:56 2025 +0200

    Begin of challenge 7

commit ca20204c8e5f287c96a322aabd45c05fa858d513
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Mon Mar 3 17:12:50 2025 +0200

    unwanted commit message

commit 86a5b719f6e3ca80a49985de75a1263794b1f8fd
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Mon Mar 3 17:17:52 2025 +0200

    Challelnge 6: Dropping Commit

commit 7b762a991413102f49d02607245a84ce107e8951 (origin/part1)
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Mon Mar 3 16:47:43 2025 +0200

    the advanced squashing

commit 785b42b262823bbf02b6472b7b133b295ee57f26
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
Date:   Fri Feb 28 12:31:45 2025 +0200

    challenge 4 done

commit 746ebefff549986c80ae912d3bb4bbeef3121ede
Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
```
### The Input
```
nothing to commit, working tree clean
Could not apply fe110c2... Chore: Create third and fourth files
gymicyerekezo@icyerekezos-iMac git_advanced % git rebase -i HEAD~14

It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr "/Users/gymicyerekezo/Documents/git_advanced/.git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.
gymicyerekezo@icyerekezos-iMac git_advanced % git rebase --skip    
Successfully rebased and updated refs/heads/challenge7.
gymicyerekezo@icyerekezos-iMac git_advanced % git log

```

## Challenge 8: Cherry-picking Commits

```
PS C:\Users\DONDOU\Desktop\git_advanced> git rebase -i HEAD~18
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting
error: could not detach HEAD
PS C:\Users\DONDOU\Desktop\git_advanced>
PS C:\Users\DONDOU\Desktop\git_advanced>
PS C:\Users\DONDOU\Desktop\git_advanced>
PS C:\Users\DONDOU\Desktop\git_advanced>
PS C:\Users\DONDOU\Desktop\git_advanced>
PS C:\Users\DONDOU\Desktop\git_advanced> git cherry-pick 3e49827 
You are currently cherry-picking commit 3e49827.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
PS C:\Users\DONDOU\Desktop\git_advanced> git cherry-pick --continue
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
PS C:\Users\DONDOU\Desktop\git_advanced> git add .
PS C:\Users\DONDOU\Desktop\git_advanced> git cherry-pick --continue
[ft/branch 5ae1ea0] Implementation of test5.md
 Date: Wed Mar 5 11:58:01 2025 +0200
 1 file changed, 1 insertion(+)
PS C:\Users\DONDOU\Desktop\git_advanced>
```

## Challenge 9: visualization Commit History (Bonus)

```

PS C:\Users\DONDOU\Desktop\git_advanced> git log --graph
* commit ddc749901f7fedd28381d24a65b93d75fad3fd1f (HEAD -> main, origin/main, origin/ft/branch, origin/HEAD, ft/branch)
| Author: dondou21 <dondouabiyi@gmail.com>
| Date:   Wed Mar 5 12:08:58 2025 +0200
|
|     Challenge 8 done (cherry-picking commit)
|
* commit 5ae1ea009c60b1e3277b929746bfd1030b30cdae
| Author: dondou21 <dondouabiyi@gmail.com>
| Date:   Wed Mar 5 11:58:01 2025 +0200
|
|     Implementation of test5.md
|
* commit 3e4982733353ff74db146a12624d47933f0bb49d
| Author: dondou21 <dondouabiyi@gmail.com>
| Date:   Wed Mar 5 11:58:01 2025 +0200
| 
|     Implementation of test5.md
|
*   commit 4e1ebecaa5b28d69f94d1e96e46d316345a03a24 (origin/challenge7, challenge7)
|\  Merge: c3473fb 168ab17
| | Author: dondou21 <dondouabiyi@gmail.com>
| | Date:   Wed Mar 5 11:41:30 2025 +0200
| |
| |     Merge branch 'main' of https://github.com/dondou21/git_advanced into challenge7
| |
| * commit 168ab17b0d14891b96b062ab3ccb55df0ac38a2f
| | Author: dondou21 <dondouabiyi@gmail.com>
| | Date:   Wed Mar 5 11:24:44 2025 +0200
| |
| |     Pull request done successfully
| |
| *   commit c41a62cf45778c1c1f63c1a0f7173d49a72ab3fb
| |\  Merge: 5574060 26560b4
| | | Author: dondou21 <dondouabiyi@gmail.com>
| | | Date:   Wed Mar 5 11:22:58 2025 +0200
| | |
| | |     Merge branch 'main' of https://github.com/dondou21/git_advanced
| | |
| | * commit 26560b48858e9fef7631a9e27b1d3f556da92434
| | | Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
| | | Date:   Mon Mar 3 17:17:52 2025 +0200
| | |
| | |     Challelnge 6: Dropping Commit
| | |
| | * commit 9d7b9eee5294c1a41fc2de1573f9e0fcb2716f26
| | | Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
| | | Date:   Mon Mar 3 17:12:50 2025 +0200
| | |
| | |     unwanted commit message
| | |   
| | *   commit bc2b32911dbefdc80d8dd3784f89a862c92290c0
| | |\  Merge: 859e61c 7b762a9
| | | | Author: Dondou <106757087+dondou21@users.noreply.github.com>
| | | | Date:   Mon Mar 3 17:03:04 2025 +0200
| | | | 
| | | |     Merge pull request #1 from dondou21/part1
| | | |
| | | |     the advanced squashing
| | | |
| | * |   commit 859e61c2d9e7f86c17a9e1b94e83e71b28341a83
| | |\ \  Merge: 785b42b a1b01cc
| | | | | Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
| | | | | Date:   Fri Feb 28 12:32:27 2025 +0200
| | | | | 
| | | | |     Merge branch 'main' of https://github.com/dondou21/git_advanced into main
| | | | |
| | | | |     The fourth challenge done
| | | | |
| | | * |   commit a1b01cc0e8ba1901fc15eaad6b6472b13643169c
| | | |\ \  Merge: 746ebef fe110c2
| | | | | | Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
| | | | | | Date:   Fri Feb 28 12:11:29 2025 +0200
| | | | | |
| | | | | |     Challenge 3 done by changing pick to squash for thr commit  Create second file
| | | | | |
| | | | * | commit fe110c2e191c7daee924470de904803429f55ce6
| | | | | | Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
| | | | | | Date:   Fri Feb 28 11:33:32 2025 +0200
| | | | | | 
| | | | | |     Chore: Create third and fourth files
| | | | | |
| | | | * | commit 2fb8e4801da81c8c8e15d6cc3afd275fccd8f2b6
| | | | | | Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
| | | | | | Date:   Fri Feb 28 11:33:32 2025 +0200
| | | | | | 
| | | | | |     chore: Create another file
| | | | | |     
| | | | | |     Change the another file to second file
| | | | | |
| | | | * | commit 021b234eae8bdca981abc41f6d966e3809cc8bb2
| | | | | | Author: Babrah <[dondouabiyi@gmail.com](mailto:dondouabiyi@gmail.com)>
| | | | | | Date:   Fri Feb 28 11:33:32 2025 +0200
| | | | | | 
| | | | | |     chore: Create initial file
| | | | | | 
| * | | | | commit 55740607f94418decca02e391541e41a9e57b14c
| | | | | | Author: dondou21 <dondouabiyi@gmail.com>

```


## Challenge 10:Understandinig Reflog (Bonus)

```
PS C:\Users\DONDOU\Desktop\git_advanced> git reflog
204e706 (HEAD -> main, origin/main, origin/HEAD) HEAD@{0}: commit: Challenge 9 done (visualozation commit history bonus)
ddc7499 (origin/ft/branch, ft/branch) HEAD@{1}: merge ft/branch: Fast-forward
4e1ebec (origin/challenge7, challenge7) HEAD@{2}: checkout: moving from ft/branch to main
ddc7499 (origin/ft/branch, ft/branch) HEAD@{3}: commit: Challenge 8 done (cherry-picking commit)
5ae1ea0 HEAD@{4}: commit (cherry-pick): Implementation of test5.md
3e49827 HEAD@{5}: commit: Implementation of test5.md
4e1ebec (origin/challenge7, challenge7) HEAD@{6}: checkout: moving from main to ft/branch
4e1ebec (origin/challenge7, challenge7) HEAD@{7}: merge challenge7: Fast-forward
168ab17 HEAD@{8}: checkout: moving from challenge7 to main
4e1ebec (origin/challenge7, challenge7) HEAD@{9}: commit (merge): Merge branch 'main' of https://github.com/dondou21/git_advanced 
into challenge7
c3473fb HEAD@{10}: pull origin: Fast-forward
a7d8fa1 HEAD@{11}: checkout: moving from main to challenge7
168ab17 HEAD@{12}: commit: Pull request done successfully
c41a62c HEAD@{13}: commit (merge): Merge branch 'main' of https://github.com/dondou21/git_advanced
5574060 HEAD@{14}: commit: README.md added
56cba11 HEAD@{15}: reset: moving to HEAD
56cba11 HEAD@{16}: commit (amend): chore: Create third and fourth files
c8af1a2 HEAD@{17}: reset: moving to c8af1a2
172f779 HEAD@{18}: reset: moving to 172f779
845fd05 HEAD@{19}: reset: moving to 845fd05
1babaf5 HEAD@{20}: rebase (abort): returning to refs/heads/main
5bc10b2 HEAD@{21}: rebase (start): checkout HEAD~2
1babaf5 HEAD@{22}: reset: moving to HEAD
1babaf5 HEAD@{23}: commit (amend): chore: Create third and fourth files
c8af1a2 HEAD@{24}: commit (amend): chore: Create third and fourth files
845fd05 HEAD@{25}: commit: chore: Create third and fourth files
172f779 HEAD@{26}: commit: chore: Create another file
5bc10b2 HEAD@{27}: commit: chore: Create initial file
22a562e HEAD@{28}: clone: from https://github.com/dondou21/git_advanced.git

```

# Part2

## Challenge 1: Feature Branch Creation
```
PS C:\Users\DONDOU\Desktop\git_advanced> git checkout -b ft/new-feature
Switched to a new branch 'ft/new-feature'
PS C:\Users\DONDOU\Desktop\git_advanced> 
```
## Challenge 2: Working on the  Feature Branch

```
S C:\Users\DONDOU\Desktop\git_advanced> git add .    
PS C:\Users\DONDOU\Desktop\git_advanced> git commit -m'Implemented core functionality for new feature'      
[ft/new-feature b8be130] Implemented core functionality for new feature
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt
PS C:\Users\DONDOU\Desktop\git_advanced> 
```



 