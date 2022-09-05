---
layout: page
title: Labs
description: Labs of the Course.
---
# Lab-0 
{:.no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


## Part 0: Virtual Machine and SSH Overview 

This part can be used to reference terms you don't know, but is not necessary for completing the lab. You should skim it.

What is Linux?

Linux is an operating system that is free to the public to download, since it was created as an open-source program. The system is based on an older OS version called UNIX. To navigate through a Linux or UNIX system, you need to type in instructions to the computer using what is called a command-line prompt (nowadays, we often use graphical user interfaces (GUIs) to click on folders instead of typing commands to find those folders). You can even download software using the command-line prompt. Later, you will learn some of the most common Linux commands.

What is Ubuntu?

It is an African word meaning "the belief in a universal bond of sharing that connects all humanity" (https://en.wikipedia.org/wiki/Ubuntu_(philosophy)).

More seriously, it is a version of Linux. Some of the most popular distributions include names like Ubuntu, Mint, Fedora, openSUSE, and Debian, though there are dozens more. Ubuntu is known for being kind to beginners with its software center and media management while Debian is less user friendly and geared towards more technically oriented users. We will be using Ubuntu for our OS. In fact, we have created an Ubuntu version specifically for this class!

What is a Virtual Machine (VM)?

A virtual machine is an application that can imitate hardware such that you can run more than one operating system on your own computer. For example, I can run Windows on a Mac computer using a virtual machine. The VM can run while my usual operating system running without requiring a reboot. It works like any other application, sitting in a window you can minimize when you want to go on Facebook and maximize when you want to work on this class again. In case you hear this terminology, the Host OS refers to your computer, while the Guest OS is the operating system you are running on the VM.

(So why do people use dual booting? Well, one reason is that VMs tend to have higher overhead, such as being slow with 3D graphics, but booting one OS at a time means that the OS can use the computer’s full speed.)


What is a kernel?

The kernel is a program that has complete control over the whole operating system. It is the first program loaded when the OS starts up, placed in a safe location in memory to prevent being overwritten. It handles all the interfacing between the hardware and software. For instance, it may take input requests from a keyboard translate them into instructions the CPU understands.

What is a shell?

It is a program that provides the user interface for the kernel. This is where you type in the commands we mentioned earlier. Just as there are various Linux versions, there are also several shell versions, such as sh, bash, csh, tcsh, and ksh. Again, these versions came about due to improvements or extra features implemented by others (e.g. bash built upon sh by adding command completion and command history). On a Mac, the shell is called the Terminal. On Windows, the analogous form is the Command Prompt.

What is SSH?

SSH (Secure SHell) is a method of remotely connecting to and running commands on another computer (“remote” meaning something far away, so we are connecting to a computer far away). It can be accessed using the ssh command in a shell (like the Mac Terminal). It lets you access the resources of another computer that you may not have on your own computer. However, you cannot use SSH without an Internet connection. Cornell makes Ubuntu computers available to computer science students, which you can access remotely with SSH.


Windows does not come with an SSH client, which means you will need to install one on your computer if you are a Windows user. The we suggest Git (or Cygwin). Git lets you use the basic Linux commands that you'll need for this class. Cygwin puts a full UNIX environment (or close to it) but it has more overhead and you do not need it.

## Part 1: VM and SSH
For this class, you will have the option of either using the VirtualBox VM to run Ubuntu or using SSH to remotely connect to a Cornell Ubuntu machine. Choose either Part 1a or Part 1b to ensure you have access to an Ubuntu machine. SSH is preferred by most of the TAs. VM is okay if SSH does not work or you don't have internet connection.

Why are going through all the trouble of setting this up?

For one, it's often very difficult to get all of the course software on the variety of different computers and operating systems that everybody brings to the class. But more importantly, we want to ensure that the everyone is working in the same environment so that we can guarantee that if it works for you, it will also work for us (and our autograder). We therefore require that you do all of your projects work on the Ubuntu environment that we set up for you, because some of the projects we will be doing later on may work differently in different environments. We want to avoid anyone submitting anything that works on their computer but then doesn't work on our machines because the environment is different.

### Part 1a: Virtual Machine Setup
For the setup:

Go to the course resources page
Follow the instructions under the Computing Environment section.
Note: On the VirtualBox website, download the VirtualBox platform packages associated with your current Operating System.
Once you have started up the OS, you can move on to part 2.
Note: It may take some time to start up.
* You can learn more about VirtualBox at https://www.virtualbox.org/manual/ch01.html

### Part 1b: SSH
SSH (Secure shell) is a method of remotely connecting to and running commands on another computer. 


## Part 2: Installing Bash and git
### Part 2a1: Install on Windows.. 
- Download the Git for Windows installer.
- Run the installer and follow the steps below:
- Click on "Next" four times (two times if you've previously installed Git). You don't need to change anything in the Information, location, components, and start menu screens.
- From the dropdown menu, "Choosing the default editor used by Git", select "Use the Nano editor by default" (NOTE: you will need to scroll up to find it) and click on "Next".
- On the page that says "Adjusting the name of the initial branch in new repositories", ensure that "Let Git decide" is selected. This will ensure the highest level of compatibility for our lessons.
- Ensure that "Git from the command line and also from 3rd-party software" is selected and click on "Next". (If you don't do this Git Bash will not work properly, requiring you to remove the Git Bash installation, re-run the installer and to select the "Git from the command line and also from 3rd-party software" option.)
- Select "Use bundled OpenSSH".
- Ensure that "Use the native Windows Secure Channel Library" is selected and click on "Next".
- Ensure that "Checkout Windows-style, commit Unix-style line endings" is selected and click on "Next".
- Ensure that "Use Windows' default console window" is selected and click on "Next".
- Ensure that "Default (fast-forward or merge) is selected and click "Next"
- Ensure that "Git Credential Manager" is selected and click on "Next".
- Ensure that "Enable file system caching" is selected and click on "Next".
- Click on "Install".
- Click on "Finish" or "Next".
- If your "HOME" environment variable is not set (or you don't know what this is):
Open command prompt (Open Start Menu then type cmd and press Enter)
Type the following line into the command prompt window exactly as shown:
setx HOME "%USERPROFILE%"

- Press Enter, you should see SUCCESS: Specified value was saved.
Quit command prompt by typing exit then pressing Enter

  [![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/339AEqk9c-8/0.jpg)](https://www.youtube.com/watch?v=339AEqk9c-8)
  
### Part 2a2: Install Bash on Mac..
The default shell in some versions of macOS is Bash, and Bash is available in all versions, so no need to install anything. You access Bash from the Terminal (found in /Applications/Utilities).

To see if your default shell is Bash type 'code' echo $SHELL in Terminal and press the Return key. If the message printed does not end with '/bash' then your default is something else and you can run Bash by typing bash

If you want to change your default shell, see this Apple Support article and follow the instructions on "How to change your default shell".

### Part 2a3: Install Bash on Mac..
The default shell is usually Bash and there is usually no need to install anything.

To see if your default shell is Bash type echo $SHELL in a terminal and press the Enter key. If the message printed does not end with '/bash' then your default is something else and you can run Bash by typing bash.


### Part 2b1: Install Git on Windows 
Git should be installed on your computer as part of your Bash install

### Part 2a2: Install  Git on Mac..
You can use brew to install git or port to install git or you install Xcode will ship with git.

Using Brew 
```sh
brew install git
```

Using port 
```sh
sudo port install git
```


### Part 2a3: Install  Git on Linux..

If Git is not already available on your machine you can try to install it via your distro's package manager. 
For Debian/Ubuntu run
```sh
sudo apt-get install git 
```
For Fedora run
```sh
 sudo dnf install git.
```

## Part3: Introducation to Git.. 
Open a new terminal window.
Print your public key:
```sh
cat ~/.ssh/id_ed25519.pub
```
It should look similar to the following (length may differ):
```sh
ssh-ed25519 AAAAC3NzaC1lZDI1N6jpH3Bnbebi7Xz7wMr20LxZCKi3U8UQTE5AAAAIBTc2HwlbOi8T your_email@example.com
```
 In your browser, go to GitHub => Settings => SSH and GPG Keys => New SSH key and add your public key.
Set the title to something that helps you remember what device the key is on (e.g. CEN214b).
 Try connecting to GitHub with SSH:
```sh
ssh -T git@github.com
```
If all went well, you should see something like:
Hi USERNAME! You've successfully authenticated, but GitHub does not provide shell access.
In the future, when cloning repos that require authentication (e.g. the private labs repo you'll create next), instead of using the HTTPS repo URL (like https://github.com/USERNAME/REPO_NAME.git), you should use the SSH repo URL instead (like git@github.com:USERNAME/REPO_NAME.git). For example, in https://github.com/cen214-student/fall22-lab0.git, the repo named fall22-lab0 is under the cen214-student user/organization, so the SSH clone URL would be git@github.com:cen214-student/fall22-lab0.git.


In this labs you can use the editor that fit with your interest Vim,atom,nano whcih is simple and beginner-friendly compared to Vim and atom. It provides a helpful list of commands at the bottom of the interface (the ^ means the Ctrl key). Ships with many UNIX distributions (e.g. macOS, Ubuntu Linux). Open with nano file.txt.
Visual Studio Code (VSCode): fancy graphical text editor. it has some pretty helpful extensions, including a Remote SSH extension that allows you to edit files over SSH in VSCode itself instead of a terminal-based editor.
Alos my favorite the Clion which is a lot another fancy text editor. 

### Part3a: Configure Git on your computer

Be sure to set up your username and e-mail from the command line.
```sh
$ git config --global user.name "Your Name"
$ git config --global user.email "your-email-used-for-github-acct@email.com"
$ git config --global color.ui "auto"
```
Please configure your text editor as well.  If you’re not sure whether you’ve already configured Git, you can list your configuration by executing git config --list.

### Part3b: Understand Git and how it works 

#### Part3b1: Create a new repository on GitHub

- To begin, sign in to your user account on GitHub.
In the upper right corner, click the + sign icon, then choose New repository. This will take you to a page where you can enter a repository name (this tutorial uses test-repo as the repository name), description, and choose to initialize with a README (a good idea!).
- It is a good idea to add a .gitignore file by selecting one of the languages from the drop down menu, though for this tutorial it will not be necessary.
- Similarly, in practice you should choose a license to that people know whether and how they can use your code.
Once you have entered a repository name and made your selection, select Create repository, and you will be taken to your new repository web page.


#### Part3b2: Git at the command line
Below you will learn a series of commands that you can run at the command line in git bash, terminal of whatever bash tool you are using. There are 2 types of commands that you will use

Bash commands: These are commands that are native to bash / shell. They allow you to navigate around your computer, explore directory structures, create and manipulate files and directories, and more. (e.g. ls, cd, mkdir, etc)

Git commands: These are commands that are specific to git and will only be available if you have git installed on your computer. Git specific commands will always started with a call to git (e.g. git status, git clone, etc)


for more you can learn from here https://maker.pro/linux/tutorial/basic-linux-commands-for-beginners


#### Part3b3: Clone your repository to your local machine
Next, clone your newly created repository from GitHub to your local computer. From your repository page on GitHub, click the green button labeled Clone or download, and in the “Clone with HTTPs” section, copy the URL for your repository.

Next, on your local machine, open your bash shell and change your current working directory to the location where you would like to clone your repository. Note that here we are using a bash command - cd (change directory).

For example, on a Unix based system, if you wanted to have your repository in your Documents folder, you change directories as follows:

```sh
cd Documents
mkdir CEN214_tabuk_your_name
cd CEN214_tabuk_your_name
```

The git clone command copies your repository from GitHub to your local computer. Note that this is a git specific command.


```sh
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```

When you run git clone repo-path-here, You should see output like:
```sh
Cloning into 'test-repo'...
remote: Counting objects: 5, done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (5/5), done.
Checking connectivity... done.
```

Note: The repository name and output numbers that you see on your computer, representing the total file size, etc, may differ from the example provided above.

To verify that your repository now exists locally, type ls in your terminal. The ls command lists the files & folders available in your current directory. You should see a directory with the same name as the repository that you created previously on GitHub.


#### Tracking changes with git add and git commit:
Next use cd to change directories using the syntax:
```sh
cd my-repo-name
```
Replace my-repo-name with the folder name of your repo (this should be your repo name - e.g. 14ers-git)
```sh
cd test-repo
```
If you list all the files in this directory (using ls -a), you should see all of the files that exist in your GitHub repository:
```sh
ls -a
```
```sh
.git  .gitignore  LICENSE  README.md
```
Alternatively, we can view the local repository in the finder (Mac), a Windows Explorer (Windows) window, or GUI file browser (Linux).
Simply open your file browser and navigate to the new local repo.

#### Edit a file in your repo
Next, open up your favorite text editor and make a few edits to the README.md file. Save your changes.
Once you are happy with your changes and have saved them, go back to your terminal window and type git status and hit return to execute the command.

```sh
git status
```
output 
```sh
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")


```

The output from git status indicates that you have modified the file README.md. To keep track of this change to this file, you need to

add the changes, then
commit the changes.
Add and commit changes
You will use the add and commit functions to add and commit changes that you make to git.

- git add: takes a modified file in your working directory and places the modified version in a staging area.
- git commit takes everything from the staging area and makes a permanent snapshot of the current state of your repository that is associated with a unique identifier.
These two commands make up the bulk of many workflows that use git for version control.

[![IMAGE ALT TEXT HERE](https://www.earthdatascience.org/images/earth-analytics/git-version-control/git-add-commit.png)]


Add files
You can add an individual file or groups of files to git tracking. To add a single file, use
```sh
git add file-name-here-with-extension
```
To add the README.md file that you just modified, you’d use:
```sh
git add README.md
```
To add ALL of the files that you have edited at the same time, you can use:
```sh
git add --all
```
Use git add --all with caution. You do not want to accidentally add things like credential files, .DS_Store files, or history files.

Commit files
Once you are ready to make a snapshot of the current state of your repository, you can use git commit. The git commit command requires a commit message that describes the snapshot / changes that you made in that commit.

A commit message should outline what changed and why. These messages

help collaborators and your future self understand what was changed and why
allow you and your collaborators to find (and undo if necessary) changes that were previously made.
If you are not committing a lot of changes, you can create a short one line commit message using the -m flag:
```sh
git commit -m "Editing the README to try out git add/commit"
```
Alternatively, if you are committing many changes, or a small number of changes that require explanation, you’ll want to write a detailed multi-line commit message using a text editor.

If you have configured git to use your favorite text editor (via git config --global core.editor your-fav-editor-here), then you can open that editor to write your commit message using the git commit command:
```sh
git commit
```
Once you save your commit message and exit the text editor, the file that you created will contain your commit message.

#### Push changes to GitHub
So far we have only modified our local copy of the repository. To add the changes to your git repo files on your computer to the version of your repository on GitHub, you need to push them GitHub.

You can push your changes to GitHub with:

```sh
git push
```
You will then be prompted for your GitHub user name and password. After you’ve pushed your commits, visit your repository on GitHub and notice that your changes are reflected there, and also that you have access to the full commit history for your repository!


## Part4: Intro to C Overview

Welcome to C! It is a programming language that was first introduced almost half a century ago but is still one of the most commonly used programming languages due to its speed, efficiency, and ability to closely interface with hardware.

Let's get to coding in C. On your Ubuntu machine (VM or SSH), open up a text editor (vim,nano,atom) and create a new file called hello.c. You can create and name the file in one step by entering the command atom hello.c. Type in the following C program (remember Insert mode):
```sh
#include <stdio.h>

int main() {
    printf("Hello world! I am [netid].\n");
    return 0;
}
```
But replace [netid] with your NetID (don't print square brackets). When you are done typing, save the file and exit the editor (remember Command mode and :wq?). Now you are ready to compile and run the program you just created! In your terminal, navigate to where you saved hello.c. Now run the command:

```sh
gcc -o sayhello hello.c
```

The C compiler (GCC) has compiled your source code hello.c into an executable named sayhello. The -o option allows us to name the resulting executable file anything we want. Without the flag, the default name given to the executable is a.out.

If this gives you any errors, make sure you are in the right working directory (use ls to confirm that hello.c is in the same directory). If you are in the right location, then you did not enter the program correctly — go back to your editor and fix the program. Otherwise, you have just compiled a C program. You can run your program by running the command:

```sh
./sayhello
```

And your program should run! It should print Hello world! I am [netid]. and do nothing else. For example, if your NetID is "abc123", then compilation and execution would look like something like this:


```sh
~$ gcc -o sayhello hello.c
~$ ./sayhello
Hello world! I am abc123.
```

What does ./sayhello mean? The command ./sayhello means, run the executable sayhello which is located in the current directory (remember . means current directory and .. mean parent directory).


## Part5: Now push your first code to Git
You should now know how to push your first C code to the github. 
