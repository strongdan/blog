---
layout: post
title: Getting Started With Magic Functions
---

<h3>Magic Functions in Jupyter Notebook</h3>

If you have any experience with the command line interpreters like BASH, you can utilize some basic CLI command-line calls in Jupyter as well. Jupyter comes with a large number of predefined functions ("magics") that utilize command-line-like syntax and are prefaced with % (line-oriented) or %% (cell-oriented). You can run `%magic` to get a list of magic functions in Jupyter Notebooks, and you'll get documentation that looks like this:

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

If you would like to know more about a specific magic function, call that function followed by a question mark, like this `%clear?` and you'll get documentation like this:

```
Docstring:
Make functions callable without having to type parentheses.

Usage:

   %autocall [mode]

The mode can be one of: 0->Off, 1->Smart, 2->Full.  If not given, the
value is toggled on and off (remembering the previous state).

...
```

<h4>Line Magics</h4>

Line magics are defined with __%__ and their arguments only span an single line. For example:
`%echo "Hello World!` will print out `"hello world"`

<h4>Cell Magics</h4>

Cell magics are defined using __%%__ and can typically only be used once per cell (though there are some exceptions). They recieve an argument from the current line (where they are defined) and from the body of the cell. Here is an example from the [documentation](http://nbviewer.jupyter.org/github/ipython/ipython/blob/1.x/examples/notebooks/Cell%20Magics.ipynb):
```
%%writefile foo.py
print('hello world')
```
This magic will create a file called foo.py and write `print('hello world')` to the file. If you type `%ls`, you'll see foo.py in your working directory. 

<h4>Other Interpreters</h4>
You can even use magics to run code in other languages' interprters. Using the `%ruby` magic, we can print to the console: 
```
%%ruby
puts "Hello from Ruby #{RUBY_VERSION}"
```
This will output 'Hello from Ruby 1.9.3'. The same sort of thing can be done using the BASH interpreter:
```
%%bash
echo "hello from $BASH"
```
This will output your bash filepath: 'hello from /usr/local/bin/bash'.
