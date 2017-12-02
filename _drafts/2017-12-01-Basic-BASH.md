---
layout: post
title: Getting Started with BASH
---

# Some Basic BASH Commands to Get You Started With the Command Line

The command line is a great way to quickly and efficiently work with files, and often it's the only way to accomplish certain tasks. If you're not already familiar with BASH (Bourne-Again SHell), this post is a very quick and dirty review of some command and shortcuts to get you started navigating your computer from the command line. Open up your terminal on macOS or any flavor of Linux (I can't guarantee this will work in Windows Powershell. Only Windows 10 has a BASH shell). 

### Some Basic Commands
**PWD** - You can also print the directory you are in using _pwd_ (print working directory): `pwd`

**LS** - View the contents of your current directory with _ls_: `ls`. You can view a long-form list with `ls -l` or view hidden files with `ls -a`. 

**TOUCH** - You can create a file using _touch_: `touch file` and then type `ls` again to view it. If you type `touch file` again, the date/time modified for that file will be updated to the time you touched it. 

**ECHO** - Start interacting with the terminal by printing to standard output using _echo_: `echo "Hello"`

You can also use _echo_ to write to file like this: `echo "Here is some text" > file2`, which will both create the file for you and write to it. If you try this again, it will overwrite your previous text. If you would like to append text to this file, you will need two _>_: `echo "Here is more text >> file`.

**CAT** - If you would like to take a look at the file you just wrote to, type `cat file2`. 

### Working With Directories
Navigate to your home directory (typically /bin/bash/user) `cd ~`

Navigate to a specific directory `cd my_directory`

Navigate up a level `cd ..`

List subdirectories `ls -d */`

Navigate up more than one level `cd ../..`

Navigate to previous directory `cd -`

Make a new directory `mkdir directory_name`

Delete an empty directory `rmdir`

Delete a directory and its contents `rmdir -rf directory_name`

### Working with Files

Read a file with less `less file.txt` or cat `cat file.txt`

Opening a file for editing in Vim `vi file.txt` or `vim file.txt`

Empty a file without deleting it `> file.txt`

Remove a file `rm file_name` or all files `rm *`

Open a file in a program using `file.txt open program_name`

Move a file `mv file_name directory_name`

Copy a file `cp file_name directory_name`

Edit a file `nano filename` or `vi filename`

Rename a file or directory `mv file.txt file2.txt`

Batch rename files `rename –v 's/foo/bar/g' *`

### Multiple Commands
In a single line `command1; command2; command3`

Run commands together `command1 && command2`

Reuse last item with `$!` eg. `cd !$`

Reuse previous command with `!!` eg. `sudo !!`

Show the history of commands used `history`

Loop Over a set of Files `for f in *.txt;do echo $f;done`

### Searching
Search commands previously used `ctrl + r`

Find a text string in files `grep -Pri search_term filepath/file.txt`

Find a file `find . –name "*.txt" –mtime 5`

Find a directory using _locate_ `locate directory`

List contents several directories deep `ls dirname /*/*`

Search text and return lines that match a pattern `egrep [command line options] <pattern> [path]`

Regular expressions

### Getting Help
Finding out how to use a command `command --help`

Finding manual pages `man` or `man command`

Search man pages using a keyword `man -k search_term`

### Working With Text
Move to end of current line `ctrl-E`

Move to beginning of current line `ctrl-A`

`Ctrl + u` Cut everything before the cursor to a special clipboard
`Ctrl + k` Cut everything after the cursor to a special clipboard
`Ctrl + y` Paste from the special clipboard that Ctrl + u and Ctrl + k save their data to
`Ctrl + t` Swap the two characters before the cursor (you can actually use this to transport a character from the left to the right, try it!)
`Ctrl + w` Delete the word / argument left of the cursor
`Ctrl + l` or `clear` Clear the screen

`Alt-b` moves back one word
`Alt-f` moves forward one word

### Redirection/Piping

`ps aux | grep init`

`ls –l | more`

### Using SHELL Scripts
`./scriptname.sh`

### Aliases

### Working with Permissions

### Filters

### Process Management



https://itsfoss.com/linux-command-tricks/?utm_source=facebook&utm_medium=social&utm_campaign=SocialWarfare

https://linuxacademy.com/blog/linux/tutorial-the-best-tips-tricks-for-bash-explained/

### Useful Links
* [Bash Shortcuts](https://www.skorks.com/2009/09/bash-shortcuts-for-maximum-productivity/)
* Ryan's Tutorial's [Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

