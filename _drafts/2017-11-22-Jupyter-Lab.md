---
layout: post
title: Introduction to Jupyterlab
---

https://medium.com/@boyanangelov/is-this-the-best-data-science-ide-jupyter-lab-review-fdd165470f13

I was pleasantly surprised to find [Jupyterlab](https://github.com/jupyterlab/jupyterlab) packaged with a new installation of Anaconda (Python 3). According to [Boyan Angelov](https://medium.com/@boyanangelov), Jupyterlab is a "true IDE for interactive computing," replete with file browser, terminal and code editor (in this case, Jupyter notebooks). To get started, you'll need Jupyter Notebook version 4.3 or later, which you can check by typing `jupyter notebook --version` in your shell. 

Probably the easiest way to get Jupyterlab is with Anaconda, but you can also install it using conda: 

```shell
conda install -c conda-forge jupyterlab
```

...or with the Python package manager:

```shell
pip install jupyterlab
jupyter serverextension enable --py jupyterlab --sys-prefix
```

There is another method of installing Jupyterlab from Github, which is outlined out on the official [markdown file](https://github.com/jupyterlab/jupyterlab). In order to start Jupyterlab, simply type `jupyter lab` in your shell, and a new session will open in your browser. JupyterLab uses CSS Variables for styling, so only the latest versions of Chrome, Safari and Firefox are supported. 

### Links

[JupyterLab Official Documentation](http://jupyterlab-tutorial.readthedocs.io/en/latest/)
