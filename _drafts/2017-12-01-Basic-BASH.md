---
layout: post
title: Getting Started with BASH
---

# A Handful of Basic Commands to Get You Started Using the Command Line

### Some Basic Commands
Print to the console `echo "Hello"`



### Working With Directories
Print the directory you are in `pwd`

Navigate to home directory (typically ) `cd ~`

Navigate to a specific directory `cd my_directory`

Navigate up a level `cd ..`

Navigate up more than one level `cd ../..`

Navigate to previous directory `cd -`

Make a new directory `mkdir directory_name`

Delete an empty directory `rmdir`

Delete a directory and its contents `rmdir -rf directory_name`

### Working with Files
List working directory contents `ls`

List subdirectories `ls -d */`

Touch a file to create it or update modified datetime `touch file.txt`

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
