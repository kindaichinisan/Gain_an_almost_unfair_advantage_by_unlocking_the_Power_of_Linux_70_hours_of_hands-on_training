# Gain an almost unfair advantage by unlocking the Power of Linux 70 hours of hands-on training. The ONLY course you need

# Section 3 Part2: Bash CLI

## 29 Bash CLI Intro
- manage files
- redirect program output into files
- use file as input to program
- use pipe to combine tools
- how bash env works
- how this influences program execution.
- configure prompt to achieve beautiful terminal

# Section 4: First Steps in the Terminal

## 30 Important: If you've already been using the Terminal
- This chapter is made for beginners in mind. If you have used Linux already, the pace might feel a bit slow.
- Thus, if you already fully understand the following commands without researching anything, please just skip this chapter:
    - ls ~/Desktop
    - cd /home/janniss/Downloads; ls
    - echo -ne "Hello\nWorld"
        - -n: No line break after
        - -e: Parse special characters (such as \n)
    - man ls

## 31 Setting up your Terminal
- Centos and Ubuntu terminal looks different.
- to confirm u r using Bash
    - echo "${BASH_VERSION}": anything above 5 is okay
    - if it returns nothing, type bash to run Bash. Need to do this everytime u open a new terminal.
    - sh: Bourne Shell ($), bash: Bourne Again Shell (username@pc_name:~$)

## 32 Outputting Text: the Command 'echo'
- echo: output text in terminal.
- use single quotes instead of double quote.
- echo -n: disable default line break at end.
- bash command is made of command, options, arguments
- e: enable backslash escapes ("\n")
- clear to clear the screen.
- can combine option: -e -n => -en or -ne

## 33 Displaying and Changing the Current Directory: the COmmands 'pwd' & 'cd'
- pwd: print working directory
- cd: change directory. Press tab for Autocomplete.
    - cd ~ or cd will navigate to home directory.
    - ..: up 1 directory
- /: root folder
- ~: user home directory

## 34 Listing Content in Directories: the Command 'ls'
- Cannot play video

## 35 Path Types: Absolute Paths vs. Relative Paths
- absolute path starts with / or ~ (which evaluate to /home/username/)
- relative path
    - ./: current directory

## 36 Executing Multiple Commands using ';'
- command1; command2(;)
- autocomplete foldername or filename only works for working directory.
- can also autocomplete command

## 37 Getting Help: 'man' and '--help'
- --help/ -h
    - ls only accepts ls --help.
- man: manual
    - man pages (documentation) must be installed on system
        - sudo unminimize
        - sudo apt install man-db
        - sudo reboot

# Section 5: First Steps with Linux

## 38 Intro
- user management
- elevating privileges with sudo
- package management

## 39 Information User Management
- In the upcoming videos, I will demonstrate how to temporarily elevate user rights to execute/run programs or commands that require higher privileges. This is helpful and sometimes even necessary - even for simple tasks such as installing additional software.
- Our goal for now is to just get going and to start using Linux. Thus, I'll now begin explaining some basics about user management - and we'll then leave it at that (for now).
- But don't worry, we have an in-depth chapter about user management later on in which we'll go through all the details! If you'd like to watch it now already, feel free to skip ahead to here.

## 40 User Management Basics: System Accounts, Regular Users, Superusers
- user can be categorized into 3 general categories:
    - system account
        - responsible for running background tasks on system such as webserver, database
        - dont have home directory
    - regular users
        - have access to own files and directories
        - cannot perform administrative tasks or access other user's file
    - superuser (root) (aka Administrator)
        - unrestricted access to entire system
        - can add/ remove users, install software
        - change configuration of system

## 41 Elevating Privileges: the Command 'sudo'
- sudo: superuser do: for temporarily elevating regular users privilege
    - sudo ls /root (regular user normally cannot access /root)
    - enter regular user password
    - some Linux OS may require to enable regular user sudo use.
- Dont do this: sudo rm -rf /etc. Else cannot boot in later

## 42 Optional [Troubleshooting]: When `sudo` does not work
- must turn user into regular user with administrative rights
- may not work well with sudo
    - create a new regular user

## 43 What is Package Management and how does it work?
- package management:
    - most linux distributions offer a centralized way to install software
    - helps to keep system up-to-date
    - many applications do not need to include their own updater (firefox, chrome)
    - slightly different for each distribution (diff implementation). But main idea remains the same.
- how it works?
    - our system connectes to centralized repo
    - centralized repo provide a list of available package (version and dependencies)
    - this list can be used to install updates, install additional tools

## 44 Updating and Installing Software in Ubuntu: apt
- Debian-based distribution (Ubuntu): use tool apt to keep system up-to-date
    - apt update: refresh the list of available package
    - apt upgrade: run a small upgrade of our system
        - small: upgrade existing package and allow the install of additional dependencies
    - if upgrade kernel, to also reboot the system.
    - apt full-upgrade or apt dist-upgrade: run a large upgrade of our system.
        - large: upgrade existing packages and remove/ install additional packages (dependencies)
            - remove unneeded packages (dependencies)
            - may break the system.
    - apt install [package_name] (eg. cowsay)
        - cowsay 'Hello'
    - apt remove [package_name]
    - apt autoremove: remove packages that are no longer needed.
        - run this if there is any error during upgrade or full-upgrade.
    - apt-get is another implementation of apt tool
        -apt-get upgrade will not install additional dependencies but apt upgrade will.

## 45 Updating and Installing Software in CentOS Stream: dnf

## 46: Extra lecture (optional) [MacOS]: How to use Bash in MacOS (Part1)

## 47 Extra lecture (optional) [MacOS]: How to use Bash in MacOS (Part2)

## 48 Making the Most of Role Plays [Beta]

# Section 6: File Management (Part 1) - Organize Files & Directories

## 49 Important: If you've already been using the Terminal/ Linux
- If you've already been using Linux and the Terminal:
- This chapter is made for beginners in mind. If you have used Linux already, the pace might feel a bit slow.
- Thus, if you already fully understand the following commands (without researching anything), please just skip the first part of this chapter and continue with this lecture here:
    => https://www.udemy.com/course/mastering-linux/learn/lecture/38127348/
- This is the list:
    - touch file.txt
    - cp file.txt other.txt
    - rm -R ~/Desktop (do not execute this!)
    - rmdir ~/Downloads

## 50 Intro
- create folders and files
- copy and move files
- delete files (dangerous). How to mitigate the danger

## 51 Introduction to Labs

## 52 Creating Files and Directories: the Commands 'touch' & 'mkdir'
- touch: create empty file, or many empty files
    - actual: modify the timestamp of existing file if file exists, else create a new file
    - use ls -l to see the modified timestamp of files
- mkdir: create a new directory
    - ls --color: to differentiate between files and folder

## 53 Moving and Copying Files: the Commands 'mv' & 'cp'
## 54 Deleting Files and Directories: the Commands 'rm' & 'rmdir'

## 55 Exercise Intro: Website File Management

## 56 Exercise: Website File Management

## 57 Solution: Website File Management

## 58 File Name Selection by Pattern Matching: Globbing with '*'

## 59 Advanced Glibbing Wildcards: '?', '[0-9]', '**'

## 60 Pitfalls of Globbing: Avoiding Traps in Pattern Matching

## 61 Download the materials for the next exercise

## 62 Exercise: Navigate a nested folder structure using Globbing

## 63 Exercise: Navigate a nested folder structure using Globbing

## 64 Exercise: Navigate a nested folder structure using Globbing

## 65 Extra lecture (optional): Sophisticated File Searching: the Program 'find'

# Section 7: File Management (Part 2) - Handle Text Files