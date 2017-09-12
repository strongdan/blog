---
layout: post
title: Getting Started With Magic Functions
---

<h3>A Quick Intro to Magic Functions in Jupyter Notebooks</h3>

If you have any experience with the command line interpreters like BASH, you can utilize some basic CLI command-line calls in Jupyter in the form of predefined functions ("magics") that utilize command-line-like syntax and are prefaced with % or %%. You can also type %automagic to call magic commands without the %.

Run `%magic` to get a list of magic functions in Jupyter Notebooks and you'll get documentation that looks like this:

```
IPython's 'magic' functions
===========================

The magic function system provides a series of functions which allow you to
control the behavior of IPython itself, plus a lot of system-type
features. There are two kinds of magics, line-oriented and cell-oriented.

...
```

One of the most useful magics is `%quickref`, which brings up a quick reference card for IPython (Jupyter), including information on magic functions:

```
IPython -- An enhanced Interactive Python - Quick Reference Card
================================================================

obj?, obj??      : Get help, or more help for object (also works as
                   ?obj, ??obj).
?foo.*abc*       : List names in 'foo' containing 'abc' in them.

...
```

If you would like a list of all magics, simply type in `%lsmagic` and you'll get this list:

```
Available line magics:
%alias  %alias_magic  %autocall  %automagic  %autosave  %bookmark  %cd  %clear  %cls  %colors  %config  %connect_info  %copy  %ddir  %debug  %dhist  %dirs  %doctest_mode  %echo  %ed  %edit  %env  %gui  %hist  %history  %killbgscripts  %ldir  %less  %load  %load_ext  %loadpy  %logoff  %logon  %logstart  %logstate  %logstop  %ls  %lsmagic  %macro  %magic  %matplotlib  %mkdir  %more  %notebook  %page  %pastebin  %pdb  %pdef  %pdoc  %pfile  %pinfo  %pinfo2  %popd  %pprint  %precision  %profile  %prun  %psearch  %psource  %pushd  %pwd  %pycat  %pylab  %qtconsole  %quickref  %recall  %rehashx  %reload_ext  %ren  %rep  %rerun  %reset  %reset_selective  %rmdir  %run  %save  %sc  %set_env  %store  %sx  %system  %tb  %time  %timeit  %unalias  %unload_ext  %who  %who_ls  %whos  %xdel  %xmode

Available cell magics:
%%!  %%HTML  %%SVG  %%bash  %%capture  %%cmd  %%debug  %%file  %%html  %%javascript  %%js  %%latex  %%perl  %%prun  %%pypy  %%python  %%python2  %%python3  %%ruby  %%script  %%sh  %%svg  %%sx  %%system  %%time  %%timeit  %%writefile

Automagic is ON, % prefix IS NOT needed for line magics.
```

If you would like to know more about a specific magic function, call that function followed by a question mark, like this `%autocall?` and you'll get documentation like this:

```
Docstring:
Make functions callable without having to type parentheses.

Usage:

   %autocall [mode]

The mode can be one of: 0->Off, 1->Smart, 2->Full.  If not given, the
value is toggled on and off (remembering the previous state).

...
```

<h3>Line Magics</h3>

Line magics are defined with __%__ and their arguments only span an single line. For example:
`%echo "Hello World!"` will print out `"Hello World!"`

<h3>Cell Magics</h3>

Cell magics are defined using __%%__ and can typically only be used once per cell (though there are some exceptions). They recieve an argument from the current line (where they are defined) and from the body of the cell. Here is an example from the [documentation](http://nbviewer.jupyter.org/github/ipython/ipython/blob/1.x/examples/notebooks/Cell%20Magics.ipynb):
```
%%writefile foo.py
print('hello world')
```
This magic will create a file called __foo.py__ and write `print('hello world')` to the file. If you type `%ls`, you'll see __foo.py__ in your working directory. 

<h3>Other Interpreters</h3>

You can even use magics to run code in other languages' interpreters. Using the `%ruby` magic, we can print to the console: 

```
%%ruby
puts "Hello from Ruby #{RUBY_VERSION}"
```

This will output 'Hello from Ruby 1.9.3'. The same sort of thing can be done using the BASH interpreter:

```
%%bash
echo "hello from $BASH"
```

This will output your BASH filepath: 'hello from /usr/local/bin/bash'.

You can also execute Python files with the .py extension and other Jupyter notebooks using the `%run` magic. Using a previous example, `%run foo.py` will print `hello world` to the console. It's also possible to write file contents to standard output using `%pycat`. If you type `%pycat foo.py`, Jupyter will return the contents of the file: `print('hello world')`.

<h3>Setting Environment Variables</h3>

`$env` allows you to manage Jupyter Notebook environment variables without having to restart the kernel. If you type `%env` without an argument, you will get a JSON list of all environment variables. You can set environment variables with `%env var=val`, where __val__ is the value you want to set the variable to. 

<h3>Timing</h3>

You can time how long a statement or expression takes to execute using `%time` and the CPU and wall clock times will be printed after execution. `%timeit` does virtually the same thing, but returns the average of the fastest three times after 100,000 runs.

<h3>Shell Commands</h3>

These aren't magic commands, but you can execute shell commands from within Jupyter by using the exclamation mark. `!ls *.csv` will list out any csv files and `!pip update numpy` will update your numpy installation. Virtually every BASH command will work using the __!__.

<h3>Defining Your Own Magics</h3>

It is possible to define custom magics, either using your own standalone functions or by using a base class from IPython (IPython.core.magic.Magics). This is a bit more advanced feature and requires some understanding of object-oriented programming in Python. If you want to know how to create custom magics, check out the [documentation](https://ipython.org/ipython-doc/3/config/custommagics.html#defining-magics).

<h3>Experiment!</h3>
This was a very quick introduction to magics and I provided only a few examples, but there are a lot more quite useful magics. Magics can also be combined to create more efficient workflows. You can write SQL queries and R code for different parts of your analysis, and you can even debug using `%debug`. Play around with magic functions on your own. You'll be impressed with what you can accomplish. 
