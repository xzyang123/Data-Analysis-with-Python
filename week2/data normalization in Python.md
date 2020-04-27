# Data normalization in Python
## Dta normalization

* Uniform the features value with different range

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/width%20height%20length.png?raw=true)

features | range
--- | ---
length | 150 - 250
width | 50 - 100
height | 50 - 100

*sometimes we may want to normalize the ranges so it could be consistent*

*by making the ranges consistent between the variables, normalization enables a fair comparison between the different features*

*making sure they have the same impact*

scale | [150,250] | [50,100] | [50,100]
---- | ---- | ---- | ----
impact | large | small | small

* **Another example helps to understand why normalization is important**

age | income
--- | ---
20 | 100,000
30 | 20,000
40 | 500,000

**Before:** Not-normalized
1. 'age' and 'income' are in different range

    *age range is from 0-100, but income range is from 0-20,000 or even higher*
    
2. hard to compare

    *income is about 1,000 times larger than age*
    
3. 'income' will influence the result more

    *when we do further analysis, like linear regression*

    *the attribute income will intrinsically influence the result more due to its large value*
    
    ***to avoid this, we can normalize these two varibles into values that range from zero to one***

age | income
--- | ---
0.2 | 0.2
0.3 | 0.04
0.4 | 1

**After:** Normalized
1. similar value range

2. similar instrinsic influence on analytical model

## Methods of normalizing data

**serveral approaches for normalization**
    
* Simple feature scaling

  *each value divied by the maxium value*
  
  *this makes the new values range between zero and one*

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/simple%20feature%20scaling.png?raw=true)

* Min-Max
  *the new ranges is between zero and one*
  
![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/min%20max.png?raw=true)

* Z-score/standard score

  *each value subtract the mu which is the average*
  
  *then, divide by the standard deviation sigma*
  
  *the resulting values are around zero, range from negative 3 and positive 3 but can be higher or lower*

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/z%20score.png?raw=true)

## Simple feature scaling in Python

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/pandas.png?raw=true)

`df['length'] = df['length']/df['length'].max()`

## Min-max in Python

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/min%20max%20in%20python.png?raw=true)

```python
df['length'] = (df['length') - df['length'].min())/
               (df['length'].max() - df['length'].min())
```

## Z-score in Python

![alt text](https://github.com/xzyang123/Data-Analysis-with-Python/blob/master/week2/images/z%20score%20in%20python.png?raw=true)

```python
df['length'] = (df['length'] - df['length'].mean()) / df['length'].std()
```








