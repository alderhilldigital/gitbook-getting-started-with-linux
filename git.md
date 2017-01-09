# Beginner's Guide to Git

One of the packages that can be installed using the package managers is git. Git is a distributed version control system that can be used to create and maintain files and directories in a repository. The repository can be copied and moved and then copies can be joined together again using git's conflict resolution. This guide is brief look at the functionality and commonly used commands  in git. If more detail is required, there is documentation available at [https://git-scm.com/docs.](https://git-scm.com/docs)

**Quick Setup and First Commit**

Any directory can be made into a git repository by initialising it. Running the initialisation command will create a hidden directory called .git. This directory contains the configuration, version references, remote references and other information used to maintain the git repository.

Initialise the first-project folder as a git repository

`git init projects/first-project`

Add all the files in the first-project directory to the git repository

`git add .`

Commit any changes that have been made to the git repository including any files that have been added or removed. The a option  \(-a\) tells git to include all files that have been modified or deleted and the m option \(-m\) is followed my a message to be added to the commit.

`git commit -am 'first commit'`

Add a remote location where the repository is stored. The following command names the remote location 'origin' but it could be called anything e.g. source. It then passes an address for the remote location.

`git remote add origin https://github.com/user/repo.git`

**Pushing, pulling and cloning**

Once you have added some files to your repository, committed the files and added a remote location you can push the files to that location.

`git push origin master`

This will take all the files from the local copy of your repository  and push them to the remote copy called 'origin' and but them in a branch called 'master'.

The remote repository can now be used by others. To get a copy of the repository a user will clone the repository to their local PC.

`git clone https://github.com/user/repo.git`

This will create a copy of the repository on the users local PC in the current folder with the name of the repository. The user can now make any changes they want and then they can commit and push those changes to the remote repository.

If a user makes changes then anyone who has a local copy of the repository can get those changes using the pull command.

`git pull origin master`

This will try an pull down any changes to the git repository since the user last pulled down changes or cloned the repository.

**Status and Conflict Resolution**

The status command will give brief description of the differenced between the current working files and the files from the last commit. It will also include any files that have been added to the the directory but not added to the repository. These are known as untracked files. To make any new files tracked, the add command must be run.

`git status`

When a user commits a change to a file and tries to pull down from a remote repository where the same file has a conflict, git will highlight that a conflict has occurred. This conflict must be rectified before the user can push their changes.

git will indicate the file with the conflict and in the file will have both sections of the file, where the conflict occurs, in sequence encapsulated by '&lt;&lt;&lt;&lt;&lt;&lt;&lt;' and '&gt;&gt;&gt;&gt;&gt;&gt;&gt;' and separated in the middle by '======='

**Example**

`<<<<<<< HEAD`

`<td> hello world </td>`

`=======`

`<td> hello me </td>`

` >>>>>>> new_change`

To resolve the conflict, the user must remove the encapsulation lines and just leave the content they wish to retain.

Once the conflict has been resolved, the file can be saved, committed and pushed to the remote repository.

