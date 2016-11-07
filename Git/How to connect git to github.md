# How to deal with the git and github

## install Git on your PC
First you go to git's [officeal site](https://git-scm.com/).

Then you [download the newest version of git](https://git-scm.com/download/win) to install on your computer.


## connect to github
After you have create a new directory and want to connect this directory to github.

You right click hte mouse and click the Git Bash here.
![Git Bash here](C:\TechniqueFile\Git\Git Bash here.png)


## Make a new repository

Make a new repository on your github that according to the new directory you went ot sync.
Here I create the new repository of "TechniqueFile"
The you use the "clone or download" button to copy the name of your repository.

![Create a repository on your github](C:\TechniqueFile\Git\Create the new repository.png)

## Connect the directory to the remote repository

First you must config your user.name and user.email
then you must connet the github with the repository name you have just copyed from github
then you set up the SSH key.

you can reference the link below to do that.
[Check for existing SSH key](https://help.github.com/articles/checking-for-existing-ssh-keys/)

[generating-a-new-ssh-key](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#adding-your-ssh-key-to-the-ssh-agent)

[adding-a-new-ssh-key](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)


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

That ssh command shows that you have import the SSH key.

## sync with the github
Then you make the git subdirectory and make a new file named "how to connect your git to github.md".

After that  you went to add all of this to github.

    $ git status
    On branch master

    Initial commit

    Untracked files:
      (use "git add <file>..." to include in what will be committed)

            Git/

    nothing added to commit but untracked files present (use "git add" to track)

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ git add -A
    warning: CRLF will be replaced by LF in Git/How to connect git to github.md.
    The file will have its original line endings in your working directory.

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ git commit -m "add git directory"
    [master (root-commit) daf7c33] add git directory
     2 files changed, 31 insertions(+)
     create mode 100644 Git/Git Bash here.png
     create mode 100644 Git/How to connect git to github.md

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ git push -u origin master
    Counting objects: 5, done.
    Delta compression using up to 4 threads.
    Compressing objects: 100% (4/4), done.
    Writing objects: 100% (5/5), 9.03 KiB | 0 bytes/s, done.
    Total 5 (delta 0), reused 0 (delta 0)
    To github.com:BJTU-zhulingxi/TechniqueFile.git
     * [new branch]      master -> master
    Branch master set up to track remote branch master from origin.

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)
    $ git log
    commit daf7c33ec08b5dcdb5ee3dba49704fb86b5f5ea6
    Author: BJTU-zhulingxi <lzxhu@bjtu.edu.cn>
    Date:   Mon Nov 7 17:28:40 2016 +0800

        add git directory

    Administrator@PC201610270942 MINGW32 /c/TechniqueFile (master)

Remember,you must use this command to push your file to github for the first time 

>git push -u origin master


when you open your github on the website,you will find the change have been made after the command.

![After push the file to github](C:\TechniqueFile\Git\After push the file to github.png)
