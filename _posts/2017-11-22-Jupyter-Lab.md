---
layout: post
title: Introduction to JupyterLab
---

## A Quick Overview of JupyterLab

I was pleasantly surprised to find [JupyterLab](https://github.com/jupyterlab/jupyterlab) packaged with a new installation of Anaconda (Python 3). According to [Boyan Angelov](https://medium.com/@boyanangelov), JupyterLab is a "true IDE for interactive computing," complete with file browser, terminal and code editor (in this case, Jupyter notebooks). The software is still in alpha preview, but appears to work quite well. To get started, you'll need Jupyter Notebook version 4.3 or later, which you can check by typing `jupyter notebook --version` in your shell. 

Probably the easiest way to get JupyterLab is with Anaconda, but you can also install it using conda: 

`conda install -c conda-forge jupyterlab`

...or with the Python package manager:

`pip install jupyterlab`
`jupyter serverextension enable --py jupyterlab --sys-prefix`

There is another method of installing JupyterLab from Github, which is outlined out on the official [markdown file](https://github.com/jupyterlab/jupyterlab). 

In order to start JupyterLab, simply type `jupyter lab` in your shell, and a new session will open in your browser. JupyterLab uses CSS Variables for styling, so only the latest versions of Chrome, Safari and Firefox are supported. 

Here's what it looks like "in the flesh":

![JupyterLab](/assets/jupyerlab.png)

You can open multiple tabs and have several Python or R kernels running side-by-side. 

![tabs](/assets/tabs.png)

JupyterLab supports a number of different programming languages:

![languages](/assets/languages.png)

There's a built-in python console

![console](/assets/console.png)

You can map keys to match your favorite text editor or IDE

![keymap](/assets/keymap.png)

Overall, I'm impressed with what JupyterLab can do, and so far I haven't discovered any limitations with this new IDE. I'm looking forward to seeing JupyterLab improve and gain functionality. I'll post any updates here on my blog. 

### Links

* [JupyterLab Official Documentation](http://jupyterlab-tutorial.readthedocs.io/en/latest/)
* [JupyterLab Tutorial](http://jupyterlab-tutorial.readthedocs.io/en/latest/)
* [npm Installation](https://www.npmjs.com/package/jupyterlab)
* [conda Installation](https://anaconda.org/conda-forge/jupyterlab)
