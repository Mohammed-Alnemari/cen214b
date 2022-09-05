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

How to SSH is explained in Part 1b.

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



Important: If you use Windows, your computer does not come with an SSH client. Skip down to "For Windows users only", then come back here to complete the process"

Choose one of the two options:

- Git
If you do not already have Git installed on your computer, install it from here. You will be able to ssh by opening the "git bash" program and using the ssh tool there. If you would like to ssh through the windows command line, follow in the instructions below.
If you do not already have Git installed, install it now.
You’ll now need to find where Git installed its ssh client. It will either be in “C:\Program Files\Git\usr\bin” or “C:\Program Files\Git\bin”. Find which of those directories contains a file called “ssh.exe”, then copy that filepath
Open Control Panel -> System and Security -> System, then click “Change Settings”. Go to “Advanced”, then click “Environment Variables”
Under “User Variables” click “Path”, then click “Edit”
Click “New”, then paste in the filepath from above (You may see just a string to edit instead - in this case simply type a semicolon separator then paste the path)
Done! Now when you open the windows command line, you will be able to ssh.

  

