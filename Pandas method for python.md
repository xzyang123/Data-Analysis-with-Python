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

**Check statistical summary of each column**

*learn about the distribution of data in each column*

* Returns a statistical summary

`df.describe()`

![alt text](https://user-images.githubusercontent.com/61488535/80266083-fd17fc00-864e-11ea-8ffe-b525092f96a4.png "Logo Title Text 1")

* Provide full summary statistics

`df.describe(include='all')`

