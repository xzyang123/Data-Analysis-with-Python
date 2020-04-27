# Binning

* convert group values into bins
* for example, bin “age” into [0 to 5], [6 to 10], [11 to 15]
* can improve accuracy of the predictive models
* from group a set of values into a smaller number of bins
* have better understanding of the data distribution

## For example

**'price' has a range from 5,000 to 45,500**

In order to have a **better representation** of price

we can categorize the price into three bins

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/price%20bin.png?raw=true)

## Binning in Python Pandas

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/bin%20in%20python.png?raw=true)

```python
bins = np.linspace(mid(df['price']), max(df['price']), 4)

group_names = ['low', 'medium', 'high']

df['price_binned'] = pd.cu(df['price'], bins, labels = group_names, include_lowest = True)
```

## Visualizing binned data

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/BINNED%20DATA.png?raw=true)







