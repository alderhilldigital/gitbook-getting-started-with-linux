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

**Status and Conflict Resolution**

