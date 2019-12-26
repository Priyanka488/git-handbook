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
