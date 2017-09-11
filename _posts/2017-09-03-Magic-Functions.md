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

<h4>Cell Magics</h4>

<h4>Line Magics</h4>

Functions that work with code: %run, %edit, %save, %macro, %recall, etc.
Functions which affect the shell: %colors, %xmode, %autoindent, %automagic, etc.
Other functions such as %reset, %timeit, %%writefile, %load, or %paste.
