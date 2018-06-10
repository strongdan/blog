---
layout: post
title: Intermediate Tasks in Bash
---

# Beyond the Basics: Some Intermediate Bash

## A Few Intermediate Commands
### grep
Although I briefly covered grep in my previous post, I didn't provide many details. Grep is used to search for a pattern within a file or multiple files. The basic format is `grep "search term" file.txt`. You can use regular expressions with grep (a topic I'll cover in a future post). This [cheat sheet](https://ryanstutorials.net/linuxtutorial/cheatsheetgrep.php) is a great place to get started with regex. There's much more to using grep than I can cover here, but if you want more information [Alvin Alexander](https://alvinalexander.com/) has a great overview [here](https://alvinalexander.com/unix/edu/examples/grep.shtml).

If you'd like to try this out, go to [https://hipsum.co/](https://hipsum.co/) and copy some meaningless text. Using _touch_, create one or more files and, using your text editor of choice (Vim, Emacs, Nano, Pico, etc.), paste in what you copied. Use grep to locate a word or pattern you know is in the file, like so:

```bash
$ grep "flexitarian" new_file.txt # this will search only within new_file.txt
```

Grep will return the line to standard output - with the keyword highlighted - from the file where it finds a match (or whichever output the user requests with options). In this example, this was my output:

_+1 meh craft beer shoreditch snackwave iPhone man bun twee polaroid keytar narwhal artisan drinking vinegar hashtag. Salvia roof party sustainable vegan woke cronut lyft pug. Gentrify flannel __flexitarian__, pickled cray plaid hammock celiac tacos cloud bread fanny pack kombucha. Scenester neutra VHS, hell of single-origin coffee cold-pressed tofu __flexitarian__ letterpress la croix banjo pork belly franzen._

If you want to search multiple files in a directory, you'll need to use the _-R_ flag (to search files recursively) like this:

```bash
$ grep -R "fingerstache" . # this will search all files in the current directory
```

### find
### more and less
### diff
### file
### head and tail
### sort

## Aliases

## Variables

## Input/Output

## Redirection

## Piping

## Pipelining

## Globbing and String Expansion

## Hard and Symbolic Links

## Modifying ~/.bashrc and ~/.bash_profile

## Using SHELL Scripts
## Working with Permissions
## Filters
## Process Management
## Regular expressions

https://code.snipcademy.com/tutorials/linux-command-line/intermediate-commands

https://jayconrod.com/posts/103/intermediate-linux-command-line-tutorial

http://etutorials.org/Linux+systems/how+linux+works/Chapter+1+The+Basics/1.5+Intermediate+Commands/

https://www.linux.com/learn/bash-201-intermediate-guide-bash
