# Descriptive Statistics

When you begin to analyze data

it's important to first explore your data before you spend time building complicated models

* Describe basic features of data

* Giving short summaries about the sample and measures of the data

## Descriptive statistics - Describe()

* summarize statistics using pandas `describe()` method

`df.describe()`

*It shows the mean, the total number of data points, the standard deviation, the quartiles, and the extreme values*

*Any NaN values are automatically skipped in these statistics*

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week3/images/describe%20().png?raw=true)

## Descriptive statistics - value_counts()

* summarize categorical data is by using the `value_counts()` method

*for example: from the previous data frame, the dirve system has a variable category, such as forward-wheel drive, rear-wheel, and four-wheel drive*

`drive_wheels_counts = df['drive-wheels'].value_counts()`

*summarize the categorical data*

`drive_wheels_counts.rename(colunms = {'drive-wheels': 'value_counts', inplace = True}`

*change the colunm name*

`drive_wheels_counts.index.name = 'drive-wheels'`

*add the index to the data frame*

&nbsp; | value_counts
--- | ---
drive-wheels | &nbsp;
fwd | 118
rwd | 75
4wd | 8

## Descriptive statistics - box plots

*The main features that the box plot shows are the median of the data, which represents where the middle data point is.*

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week3/images/box%20plot.png?raw=true)
















