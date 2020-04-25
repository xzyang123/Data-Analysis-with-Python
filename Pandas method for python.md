## Before any analysis you need to check:

* Data Types
* Data Distribution

## Data Types

Pandas Types | Native Python Types | Description
--- | --- | ---
object | string | numbers and strings
int64 | int | Numeric characters
float64 | float | numeric characters with decimals
datatime64, timedelta[ns] | N/A | time data

**Why check data types?**
* potential info and tpye mismatch
* compatibility with python methods

**How to check data types**

`df.dtypes`

## Data Distribution

**Check statistical summary of each column**

*learn about the distribution of data in each column*

* Returns a statistical summary

`df.describe()`

![alt text](https://user-images.githubusercontent.com/61488535/80266083-fd17fc00-864e-11ea-8ffe-b525092f96a4.png)

* Provide full summary statistics

`df.describe(include='all')`

![alt text](https://user-images.githubusercontent.com/61488535/80266191-86c7c980-864f-11ea-8895-66fbf4c9751f.png)

* Provide top 30 rows and bottom 30 rows of the dataframe

`df.info()`

![alt text](https://user-images.githubusercontent.com/61488535/80266315-00f84e00-8650-11ea-9f93-2c322ddba406.png)
