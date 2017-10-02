---
layout: post
title: A few basic statistical tests using SciPy
---

<h3>A Quick Refresher on Statistics in Pandas and SciPy</h3>

Like most of us, you may have forgotten most of the details from that mandatory introductory stats class you took in college. Don't worry - I'll give you a quick refresher here. We'll cover some basic statistical tests, when you might want to use them and what the results mean. 

```
import scipy as sp
from scipy import stats
import numpy as np
```

# Descriptive Statistics

```x = sp.randn(1000)```

* Mean: ```x.mean()```
* Median: ```x.median()```
* Minimum: ```x.min()```
* Maximum: ```x.max()```
* Variance: ```x.var()```
* Standard Deviation: ```x.std()```
* Skew : ```x.skew()```
* Kurtosis: ```kurt()```

# Probability Distributions

Continuous probability distributions:

* norm : Normal or Gaussian
* chi2 : Chi-squared
* t : Student’s T-test
* uniform : Uniform

Discrete probability distributions:

* binom : Binomial
* poisson : Poisson

Examples of statistical functions:

* mode : Modal value
* moment : central moment
* describe: descriptive statistics
* histogram: histogram of data


https://www.datacamp.com/community/tutorials/statistics-python-tutorial-probability-1#gs.XCU0Z14
