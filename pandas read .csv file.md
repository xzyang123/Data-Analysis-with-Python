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

`df` 可以打印整个dataframe但是对于大容量文件而言很费时
`df.head(n)` show first *n* rows
`df.tail(n)` show bottom *n* rows
