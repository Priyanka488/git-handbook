# git-handbook
Just so that I don't forget the git commands ! 

## 1. Git init
The command is used to initialise a local repo as git repo.
``` git init```

## 2. Git clone

To clone a repo :

``` git clone <URL>```

To clone a repo in a directory with a different name

``` git clone <URL> dir-name ```

At this point of time, you must be having a Git repo on your local machine, and a checkout/ working-copy of all the files.<br>
So now, you make changes.<br>
And at any point you wish to record the state of the project, you <b>commit the snapshot of those changes</b><br>
<br>

### States of a File :

1. <b>Tracked</b> - the files that  Git knows about, can be modified, unmodified or staged.
2. <b>Untracked</b> - any file that wasn't present in your last snapshot.

Note : Initially, all files are tracked and unmodified.Once you make changes to any file, Git marks them as modified (since it has changed in comparison to the last commit), and then as you work, you selectively stage the modified files and commit the staged changes. And the cycle repeats !<br>

Untracked  -> Staged (Add the file)<br>
Unmodified -> Modified (Edit the file)<br>
Modified -> Staged (Stage the file )<br>
Staged -> Unmodified (Committed the file)<br>
Unmodified -> Untracked (removed the file)<br>

## 3. Git Status

used  to determine which files are in which state.

``` git status 
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```

Means -
1. Tells that you are on the branch master.
2. Informs that the the branch has not diverged from the same branch on the server.
3. Clean working directory - meaning by that none of the tracked files have been modified.
4. If it shows "Changes to be committed:" then it means that the following files have been staged.
5. If it shows "Changes not staged for commit :" means that a file that is tracked has been modified in the working directory but not yet staged. To stage it, you run the ```git add``` command.
5. If it shows "Untracked files", then you can track/stage it using ```git add```.

## 4. Git add

used to track new files.

``` git add  <file-name>```

Once you run ```git add``` on a file, it gets tracked and staged.

Basically, ``` git add``` is a multipurpose command, you use it to begin tracking new files, to stage files, and to do other things like marking merge-conflicted files as resolved. It may be helpful to think of it more as “add precisely this content to the next commit” rather than “add this file to the project”.

Note : Git stages a file exactly as it is when you run the git add command. So, If you modify a file after you run git add, you have to run git add again to stage the latest version of the file.

Suppose, you modified a file after running git add, and do ```git status```, the file name will be shown both under the staged section, as well as the unstaged section. And in case you do, ```git commit``` from here , the state of the file on that previous git add gets committed , and not the current state.

So, to get the current state of the file to get committed, you must run  ``` git add ``` again.

