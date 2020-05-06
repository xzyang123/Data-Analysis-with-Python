# GroupBy in Python

## Purpose

relationship between the different types of drive system, forward, rear, and four-wheel drive, and the price of the vehicles?

which type of drive system adds the most value to a vehicle?

      if we could group all the data by the different types of drive wheels 

      and compare the results of these different drive wheels against each other.
      
## Groupby() - Example

Finding the **average price of vehicles** and observe how they differ between **different types of body style**s and **drive wheels** variables.

```python
df_test = df[['drive-wheels', 'body-style', 'price']]
df_grp = df_test.groupby(['drive-wheels', 'body-style'], as_index = False).mean()
df_grp
```

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week3/images/groupby.png?raw=true)

**But, this table is not easy to understand, we can transform the table to a pivot table**

## Pandas method - Pivot()

```df_pivot = df_grp.pivot(index = 'drive-wheels', columns = 'body-style')```

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week3/images/pivot.png?raw=true)

### Another way to present pivot table - Heatmap ###

` I don't like this plot, looks so complicate and difficult to understand, maybe it's useful in some conditions `

```python
plt.pcolor(df_pivot, camp = 'RdBu')
plt.colorbar()
plt.show()
```

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week3/images/heatmap.png?raw=true)




