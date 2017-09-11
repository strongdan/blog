---
layout: post
title: Getting Started With Magic Functions
---

If you have any experience with the command line interpreters like BASH, you can utilize some basic CLI command-line calls. Jupyter Notebooks come with a large number of predefined functions ("magics") that utilize command-line-like syntax and are prefaced with % (line-oriented) or %% (cell-oriented). You can run `%magic` to get a list of magic functions in Jupyter Notebooks, and you'll get documentation that looks like this:

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
