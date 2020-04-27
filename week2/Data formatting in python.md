# Dta formatting in Python

## Data formatting

* Data are usually collected from different places and stored in different formats.

* Bringing data into a common standard of expression allows users to make meaningful comparison

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/data%20formatting.png?raw=true)

## Applying calculation to an entire column

* convert 'mpg' to 'L/100km' in car dataset

*Maybe someone who lives in a country that uses metric units*

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/mpg%20to%20Lkm.png?raw=true)

`df['city-mpg'] = 235/df['city-mpg']`

`df.rename(columns = {'city-mpg': 'city-L/100km'}, inplace = True)`

## Incorrect data types

* sometimes you may find out that the data type is incorrect

*for example: the 'price' type is assigned to 'object' which should be 'flout' or 'int'*

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/incorrect%20data%20type.png?raw=true)

## Data types in Python and Pandas

*For example*

* Objects: 'A', 'Hello'.... (**letters or words**)
* Int64: 1, 3, 5 (**integers**)
* Float64: 2.123... (**real numbers**)

## Correcting data types

**To *identify* data types:**

* Use `dataframe.dtypes()` to identify data type

**To *convert* data types:**

* Use `dataframe.astype()` to convert data type

*Example: convert data type to 'int' in column 'price'*

`df['price'] = df['price'].astype('int')`
