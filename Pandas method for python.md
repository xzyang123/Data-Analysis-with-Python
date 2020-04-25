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

`df.describe()`

