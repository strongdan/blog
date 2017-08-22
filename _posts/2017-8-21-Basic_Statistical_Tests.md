---
layout: post
title: A few basic statistical tests using SciPy
---

import scipy as sp
from scipy import stats
import numpy as np

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


