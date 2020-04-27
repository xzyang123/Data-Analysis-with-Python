# Dealing with missing values in python
* Missing values occur when no data value is stored for a variable in an observation
* Often represented as '?', 'N/A', o or just a blank cell

# How to deal with missing data?
* check with the data collection source
* remove the data where missing value is found
  1. drop the variable
  2. drop the data entry
* Replace the missing values
  1. replace it with an average
  2. replace it by frequency (if the variable values are not numbers)
  3. replace it based on other functions
* Leave it as missing data

# How to drop missing values in Python
* Use `dataframes.dropna()`:
![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/drop%20missing%20values.png?raw=true)

**Remove the cars that don't have the list price**

`df.dropna(subset = ['price'], axis = 0, inplace = True)`

`inplace = True` *allows the modification to be done on the data set directly*

**Equivalent to:**

*but it does not change the dataframe*

`df = df.dropna(subset = ['price'], axis = 0)`

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/inplace.png?raw=true)

# How to replacing missing values in Python

* Use `dataframe.replace(missing_value, new_value)`:

*replace the missing value (NaN) with the mean of the column*

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/replace%20missing%20value.png?raw=true)

1. Caculate the mean: `mean = df['normalized-losses'].mean()`
2. Replace the value: `df['normalized-losses'].replace(np.nan, mean)`

*Note: 'np.nan' this 'np' means 'numpy'*

*For example:*

`import numpy as np`

`np.nan`




