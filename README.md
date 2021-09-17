# test
[maoruoxi520@22:10:54]~/workspace/test$ cat A.txt a1
a2
[maoruoxi520@22:11:20]~/workspace/tests echoa3>A.txt
[maoruoxi520@22:11:41]~/workspace/test$ git add A.txt
[maoruoxi520@22:11:58]~/workspace/test$ echo'a4>>A.txt
[maoruoxi520@22:12:13]~/workspace/test$ git status
 On branch release
Your branch is ahead of 'origin/release' by 4 commits.(use "git push" to publish your local commits)
Changes to be committed:
(use"git reset HEAD <file>..." to unstage)
modified: A.txt
Changes not staged for commit:
(use"git add <file>..." to update what will be committed)
(use "git checkout--<file>..."to discard changes in working directory)
modified:A.txt
[maoruoxi520@22:12:20]~/workspace/test$ 

[maoruoxi520@22:13:29]~/workspace/test$ cat A.txt 
a1 
a2 
a3
 a4
[maoruoxi520@22:13:35]~/workspace/test$ 
[maoruoxi520@22:14:01]~/workspace/test$ git diff A.txt diff -git a/A.txt b/A.txt index 2cdcdb0..d418277100644 a/A.txt+++ b/A.txt
@@-1,3 +1,4@ a1 a2 a3+a4
[maoruoxi520@22:14:09]1~/workspace/tests 

[maoruoxi520@22:21:28]~/learnGit$  git log --oneline --graph --all
* a8cc7d9 (HEAD -> testing) add b.txt
| * 4305959 (master) add a3
| * 2a06c56 add a2
|/  
* 89b3021 add a1
* a58d8ce init
 
 
[maoruoxi520@22:21:32]~/learnGit$ git checkout master 
Switched to branch 'master'
Your branch is ahead of 'origin1/master' by 5 commits.
  (use "git push" to publish your local commits)
[maoruoxi520@22:22:17]~/learnGit$  git log --oneline --graph --all
* a8cc7d9 (testing) add b.txt
| * 4305959 (HEAD -> master) add a3
| * 2a06c56 add a2
|/  
* 89b3021 add a1
* a58d8ce init
 
 
[maoruoxi520@22:22:31]~/learnGit$ git checkout 2a06c56
Note: checking out '2a06c56'.
You are in 'detached HEAD' state.
HEAD is now at 2a06c56... add a2
[maoruoxi520@22:22:47]~/learnGit$  git log --oneline --graph --all
* a8cc7d9 (testing) add b.txt
| * 4305959 (master) add a3
| * 2a06c56 (HEAD) add a2
|/  
* 89b3021 add a1
* a58d8ce init
 
[maoruoxi520@22:22:49]~/learnGit$ git checkout a8cc7d9
Previous HEAD position was 2a06c56... add a2
HEAD is now at a8cc7d9... add b.txt
[maoruoxi520@22:23:06]~/learnGit$  git log --oneline --graph --all
* a8cc7d9 (HEAD, testing) add b.txt
| * 4305959 (master) add a3
| * 2a06c56 add a2
|/  
* 89b3021 add a1
* a58d8ce init
 
[maoruoxi520@22:23:09]~/learnGit$ git checkout testing
Switched to branch 'testing'
[maoruoxi520@22:23:24]~/learnGit$  git log --oneline --graph --all
* a8cc7d9 (HEAD -> testing) add b.txt
| * 4305959 (master) add a3
| * 2a06c56 add a2
|/  
* 89b3021 add a1
* a58d8ce init
[maoruoxi520@22:23:27]~/learnGit$

[maoruoxi520@23:17:43]~/learnGit$ ls
a.txt
[maoruoxi520@23:17:56]~/learnGit$ cat a.txt 
a1
a2
a3
[maoruoxi520@23:18:00]~/learnGit$ git log --oneline
4305959 (HEAD -> master) add a3
2a06c56 add a2
89b3021 add a1
a58d8ce init
[maoruoxi520@23:18:15]~/learnGit$
[maoruoxi520@23:18:15]~/learnGit$ echo 'a4' >> a.txt 
[maoruoxi520@23:19:33]~/learnGit$ git add a.txt 
[maoruoxi520@23:19:43]~/learnGit$ git status 
On branch master
Your branch is ahead of 'origin1/master' by 5 commits.
  (use "git push" to publish your local commits)
