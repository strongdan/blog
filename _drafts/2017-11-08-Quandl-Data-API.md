---
layout: post
title: Using Quandl Data and API
---

### Using Quandl for Financial and Economic Data

[Quandl](https://www.quandl.com/) is a repository of data for investment professionals, and they have a stunning 20 million datasets from more than 500 sources. Their API is free to use unless you want access to "premium" datasets. They provide extensive [documentation](https://docs.quandl.com/) for their API and how to use different languages to access their data. In this post, I'm going to cover the basics of accessing Quandl data using their API and Python module.

It's pretty simple to install the Quandl library for Python from the command line with:

```python
pip install quandl
import quandl
``` 

or 

```python
pip3 install quandl
import quandl
```

The next order of business is to [sign up for a Quandl account](https://www.quandl.com/users/login) and set an API key.

```python
quandl.ApiConfig.api_key = "YOURAPIKEY"
```
For a full (searchable) list of data products Quandl offers, you can check [here](https://www.quandl.com/search?query=), but the [Data Organization page](https://docs.quandl.com/docs/data-organization) provides, shall we say, a bit more organized look at the available tables. You'll need to locate the Quandl code for the dataset you wish to retrieve via the API. For example, the currency exchange rate time series for the USA and Japan has a Quandl code of [CUR/JPY](https://www.quandl.com/data/CUR/JPY). You can download an entire time series data set using `quandl.bulkdownload("CUR/JPY")`, but there are also methods for parsing data prior to retrieval. You can specify a date range using the _start_date_ and _end_date_ arguments: `mydata = quandl.get("CUR/JPY", start_date="2016-06-15", end_date="2016-06-30")`. Here is what the requested data looks like:

```
                  RATE
DATE                  
2016-06-15  105.941000
2016-06-16  104.663100
2016-06-17  104.300001
2016-06-18  104.205800
2016-06-19  104.168200
2016-06-20  104.235501
2016-06-21  104.573700
2016-06-22  104.468400
2016-06-23  105.532701
2016-06-24  102.837901
2016-06-25  102.403899
2016-06-26  102.243799
2016-06-27  101.893199
2016-06-28  102.524101
2016-06-29  102.646501
2016-06-30  102.712900
```

You can even request a certain number of rows with the optional _rows_ argument: `data = quandl.get("CUR/JPY", rows=5)`. Quandl additionally provides a _returns_ argument that returns a Numpy array: `data = quandl.get("CUR/JPY", returns="numpy")`. Quandl allows you to perform some basic calculations on the data, like so: `data = quandl.get("FRED/GDP", transformation="rdiff")`.

It's also possible to use cell magics to create a curl request from within a Jupyter notebook like so:

```
!curl "https://www.quandl.com/api/v3/datasets/FRED/GDP.csv?collapse=annual&rows=6&order=asc&column_index=1&api_key=YOURAPIKEY"
```

In order to write this command, simply concatenate the following: (1) the requested data set URL with (2) the number of rows, (3) the sorting order, (4) the column index, and (5) the user's API key. You can find more details on the elements of this call [here](https://docs.quandl.com/docs/quick-start-examples-1). Not all of these parameters are required. 

Links
Full list of [time series parameters and table transformations](https://docs.quandl.com/docs/parameters-2)
