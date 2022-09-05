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






