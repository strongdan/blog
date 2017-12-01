---
layout: post
title: Getting Started with BASH
---

# A Handful of Basic BASH Commands to Get You Started Using the Command Line

### Navigating Between Directories
Print the directory you are in `pwd`

Navigate to home directory (typically ) `cd ~`

Navigate up a level `cd ..`

Navigate up more than one level `cd ../..`

Navigate to previous directory `cd -`

### Working with Files
List working directory contents `ls`

Touch a file to create it or update modified datetime `touch file.txt`

Read a file with less `less file.txt` or cat `cat file.txt`

Opening a file for editing in Vim `vi file.txt` or `vim file.txt`

Empty a file without deleting it `> file.txt`

Open a file in a program using `file.txt open program_name

### Multiple Commands
In a single line `command1; command2; command3`

Run commands together `command1 && command2`

Reuse last item with `$!` eg. `cd !$`

Reuse previous command with `!!` eg. `sudo !!``

### Searching
Search commands previously used `ctrl + r`

Find files with particular text using grep `grep -Pri search_term filepath/file.txt`

### Getting Help
Finding out how to use a command `command --help`

Finding manual pages `man` or `man command`





https://itsfoss.com/linux-command-tricks/?utm_source=facebook&utm_medium=social&utm_campaign=SocialWarfare
