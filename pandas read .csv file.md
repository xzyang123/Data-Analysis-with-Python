## importing a CSV file with a header

```python
import pandas as pd
url = '***************'
df = pd.read_csv(url)
```

## importing a CSV file without a header

```python
import pandas as pd
url = '***************'
df = pd.read_csv(url, header = None)
```

## Printing the dataframe in python

`df` show the entire dataframe but it costs time

`df.head(n)` show first *n* rows

`df.tail(n)` show bottom *n* rows

## Adding hearders

Replace default header `df.columns = headers`

* First, you need to assign the new headers.
  
  headers = ['xx', 'xx', 'xxx',.....]
  
## Exporting a Pandas dataframe to CSV

Save dataset using

`path = 'C:\Windows\...\automobile.csv'`
`df.to_csv(path)` 

## Exporting to different formats in Python

![alt text](http://url/to/img.png)
