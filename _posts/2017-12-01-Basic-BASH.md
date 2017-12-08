---
layout: post
title: Getting Started with BASH
---

# Some Basic BASH Commands to Get You Started Using the Command Line

This is a beginner-oriented post intended to get you comfortable using your \*nix-based operating system's command line for commond tasks. More advanced features will be the topic of future posts. 

![](https://static.pexels.com/photos/207580/pexels-photo-207580.jpeg)

The command line is a great way to quickly and efficiently work with files, and sometimes it's the only way to accomplish certain tasks. Being able to use the command line to quickly create and modify files is essential for developers in nearly every field. 

If you're not already familiar with BASH (Bourne-Again SHell), this post is meant to get you started navigating your computer from the command line. I cover some basic command and shortcuts here, but you'll want to experiment on your own and follow the links I provide at the bottom if you would like to accomplish more advanced tasks.  

If you want to follow along, open up your terminal on macOS or any flavor of Linux (I can't guarantee these commands will work with Windows Powershell. FYI only Windows 10 has a BASH shell). 

![](https://static.pexels.com/photos/33234/nautilus-shell-shimmer-silver.jpg)

### Some Basic Commands
There are a handful of bash commands you will use often, so let's get familiar with them right off the bat. 

* **`pwd`** - You can also print the directory you are in using _pwd_ (print working directory)

* **`ls`** - View the contents of your current directory with _ls_. You can view a long-form list with `ls -l` or view hidden files with `ls -a`. 

* **`touch`** - You can create a file using _touch_: `touch file` and then type `ls` again to view it. If you type `touch file` again, the date/time modified for that file will be updated to the time you touched it. 

* **`echo`** - Start interacting with the terminal by printing to standard output using _echo_: `echo "Hello"`. 
You can also use _echo_ to write to file like this: `echo "Here is some text" > file2`, which will both create the file for you and write to it. If you try this again, it will overwrite your previous text. If you would like to append text to this file, you will need to use _>>_ like this: `echo "Here is more text >> file`.

* **`cat`** - If you would like to take a look at the file you just wrote to, type `cat file2`. 

#### To practice using these commands, you can follow these steps in your interpreter:
1. Open your command line interpreter and print your working directory to get oriented
2. List the contents of the directory you're in
3. Create a few new files and then list the contents of your directory again
4. Type "hello world" or something equally silly to standard output
5. Write some text to a file and look at the file's contents in the terminal
6. List files using long (`-l`) argument, touch an existing file, then list files again to see if modified date has changed

### Working With Directories
**`cd`** is the command used to change directories. It takes one parameter - the absolute or relative filepath you would like to move to (_cd_ with no parameters takes you to your home directory).

* **`cd ~`** Navigate to your home directory (typically /bin/bash/user) `cd ~`

* Navigate to a specific directory `cd my_directory`

* Navigate up a level `cd ..`

* Navigate up more than one level `cd ../..`

* Navigate to previous directory `cd -`

* **`mkdir`** Make a new directory `mkdir directory_name`

* **`rmdir`** Delete an empty directory `rmdir directory_name`

* Delete a directory and its contents `rmdir -rf directory_name`

* List subdirectories `ls -d */`

* **`ctrl + r`** Search commands previously used 

#### Practice these commands by following along:
1. Move to your home directory and print the directory name
2. List the contents of your home directory and move to a subdirectory
3. Move back to where you were (home directory) and list all subdirectories
4. Navigate to a directory several folders deep, then return using the absolute path of your home directory
5. Create a subdirectory "new_dir" and delete it. Check that it's gone by listing the parent directory contents
6. Create a subdirectory "my_dir" and add files or folders to it, then delete it

### Working with Files
Although files and directories are technically the same thing in \*nix operating systems, some different commands are used for working with files. 

* **`less`** and **`cat`** Read a file with less `less file.txt` or cat `cat file.txt`
Less is a file reader that returns a single screen at a time and allows the user to scroll through the file. Cat is short for concatenate, and outputs results to standard output, and it can be used to quickly view the contents of files as long as you don't need to scroll.

* **`>`** Empty a file without deleting it `> file.txt`

* **`rm`** Remove a file `rm file.txt` or all files `rm *`

* **`mv`** Move a file `mv file_name directory_name`
You can also use mv to rename a file or directory like this: `mv file.txt file2.txt`. If you'd like to batch rename files, use _rename_: `rename –v 's/foo/bar/g' *`

* **`cp`** Copy a file `cp file_name directory_name`

* **`open`** Open a file using the default program with `open file.txt` or with a specific program `program_name open file.txt` (eg. `nano open file.txt`).

#### Text Editors - Vim, Emacs, Nano, Pico 
Linux and Unix provide an abundance of different text editors, each of which is extremely feature-rich. I can't tell you which ones are best, but I like using Vim. Beginners will likely appreciate the ease of getting started with nano or Emacs. 

* **`nano`** or **`pico`** Edit a file `nano filename` or `pico filename`. Nano is a clone of Pico, and both have similar functionality.

* **`vi`** or **`vim`** Opening a file for editing in Vim `vi file.txt` or `vim file.txt`
Vi is a text editor created in the 1970s for Unix and was cloned and augmented in 1991. It's a bit tricky to learn, but once you do, you'll likely be hooked. It's quite powerful and extensible. Follow the official [tutorial](http://vimdoc.sourceforge.net/htmldoc/usr_02.html) to get started with Vim. Just remember, to close Vim you will need to be in edit mode (hit escape if you aren't) and type `:q!` to quit without changes or `:wq` to write changes to file and quit (SHIFT-z-z does the same thing).

* **`emacs`** You can also edit files in GNU Emacs in the same way as Vim `emacs file.txt`
Emacs is another text editor, which I have yet to use much. There are many people who love it, and it has some additional functionality that Vim doesn't have by default, so it might be worth checking out. 

#### If you would like to try these commands out for yourself, follow along:
1. Create a file "my_file" and type or paste in some text. [Hipster Ipsum](https://hipsum.co/) is a good source for nonsense text
2. Use _less_ and _cat_ to read to the file's contents. Empty the file you created, then delete it
3. Create a new file "file.txt" and rename it to "file1.txt"
4. Create several text files, then rename them using _rename_
5. Open one of these files from the command line using your IDE of choice. Type in some text then save and close
6. Reopen the last file using nano or pico and modify it
7. Reopen the last file again using Vim or Emacs, make some changes and exit
8. Play around by adding hipster ipsum text to each of the files you created and cat the results to standard output

### Working With Text
There are a few handy shortcuts that will save you a lot of time and energy in the command line.

* **`ctrl-A`** Move to beginning of current line 
* **`ctrl-E`** Move to end of current line 
* **`Alt-b`** moves back one word
* **`Alt-f`** moves forward one word
* **`Ctrl + u`** Cut everything before the cursor to the clipboard
* **`Ctrl + k`** Cut everything after the cursor to the clipboard
* **`Ctrl + y`** Paste from the clipboard that `Ctrl + u` and `Ctrl + k` save their data to
* **`Ctrl + t`** Swap the two characters before the cursor 
* **`Ctrl + w`** Delete the word to the left of the cursor
* **`Ctrl + l`** or `clear` Clear the screen

### Searching
There are a ton of handy ways to search using the command line, which I can almost guarantee will come in super handy at some point

* **`find`** Find a file `find . –name "*.txt"`

* **`locate`** Find a directory using _locate_ `locate directory`

* **`grep`** Find a text string in files `grep -Pri search_term filepath/file.txt`

* **`egrep`** Search text and return lines that match a pattern `egrep [command line options] <pattern> [path]`

#### For practice searching, try these steps:
1. Search for one of the files you created previously using find
2. Search for a directory you know exists
3. Search for for some of the hipster ipsum you previously pasted using grep and egrep

### Multiple Commands and Command Reuse
You can also string commands together on a single line, either separately or in conjunction

* In a single line `command1; command2; command3`

* Run commands together `command1 && command2`

* **`$!`** Reuse last item with `cd !$`

* **`!!`** Reuse previous command `sudo !!`

* **`history`** Show the history of commands used 

* Loop Over a set of Files `for f in *.txt;do echo $f;done`

### Getting Help
Bash provides extensive documentation for each all commands, all of which can be accessed from the command line

* **`help`** Finding out how to use a command `command --help`

* **`man`** Finding manual pages `man` or `man command`

* Search man pages using a keyword `man -k search_term`

### Other Topics
This was a super brief and superficial orientation to the command line. There is a ton more to learn. In a future post, I will cover some more super handy shell features, including: 

* Redirection/Piping
* Using SHELL Scripts
* Aliases
* Working with Permissions
* Filters
* Process Management
* Regular expressions

### Useful Links
* [Bash Shortcuts](https://www.skorks.com/2009/09/bash-shortcuts-for-maximum-productivity/)
* Ryan's Tutorial's [Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
* [Free Code Camp Post on the Command Line](https://medium.freecodecamp.org/conquering-the-command-line-f85f5e46c07c)
