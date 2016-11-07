# How to deal with the git and github

## install Git on your PC
First you go to git's [officeal site](https://git-scm.com/).

Then you [download the newest version of git](https://git-scm.com/download/win) to install on your computer.


## connect to github
After you have create a new directory and want to connect this directory to github.

You right click hte mouse and click the Git Bash here.
![Git Bash here](C:\TechniqueFile\Git\Git Bash here.png)

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ git init
    Reinitialized existing Git repository in C:/TechniqueFile/.git/

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ git config --global user.name "BJTU-zhulingxi"

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ git config --global user.email "lzxhu@bjtu.edu.cn"

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ ssh -T git@github
    ssh: Could not resolve hostname github: Name or service not known

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ ssh -T git@github.com
    Hi BJTU-zhulingxi! You've successfully authenticated, but GitHub does not provide shell access.
