---
layout: post
title: Jupyter data.world Jump Start
---
from: https://www.dataquest.io/blog/datadotworld-python-tutorial/

![Jupyter Logo](assets/main-logo.svg)

This is a super quick introduction to using Jupyter Notebooks for Pandas tasks, although it's quite capable in other languages as well. Jupyter works particularly well with R, for example. For the sake of brevity, I will briefly go over reading in a file using the data.world API, doing some basic data cleaning and visualizing the data using a Jupyter Notebook. I use a [data.world](https://data.world/) dataset to demonstrate the ease of accessing and modifying [data.world](https://data.world/) data from within Jupyter.

Jupyter (JUlia, PYThon and R) Notebooks are an incredible resource for data analysis and visualization, whether you use R or Python... or some other crazy language. The notebooks are a great way to share code and create tutorials because they meld markup and other rich text elements with Python code that can be run within the notebook. A number of data visualization libraries work quite well in Jupyter. I’m just beginning to discover the power of Jupyter Notebooks, and frankly I'm super excited to share what I've learned. Below I provide a quick overview of how to get started using a data.world data set:

* You can install Jupyter from the command line by typing `pip3 install jupyter`. Jupyter also comes as part of an Anaconda install. If you just want to check out a demo version, go to [try.jupyter.org](https://try.jupyter.org/). 

* Jupyter notebooks are run from a local server which you launch using the terminal (or Powershell on Windows): `jupyter notebook`. An optional third parameter is used to indicate the directory to open the server from. If you'd prefer to work solely online, CoCalc (formerly Sage Math Cloud) works well for most Pandas and Numpy tasks, but you're limited on the libraries you can install. IBM also offers the [Data Scientist Workbench](https://datascientistworkbench.com/), which I feel is a bit clunky and slow. It does offer some pretty powerful analytics products, including Zeppelin Notebooks and RStudio IDE, so if you don't mind 2-3 minute setup times feel free to take advantage of IBM's free service. 

![Server]()

* When you first run your server, your default browser will open up at <b>localhost:8888</b> showing the file structure of your default directory. You can create new Jupyter (formerly IPython) notebooks by clicking the <b>New</b> dropdown on the top right. I typically choose to create a Python [default] notebook.

* Notebooks are made up of cells, which can contain Python (or a variety of other languages) code, math equations, graphs or markdown. 

Data.world has their own API


`pip install git+git://github.com/datadotworld/data.world-py.git`

`import datadotworld as dw`

`lds = dw.load_dataset('data-society/the-simpsons-by-the-data')`
