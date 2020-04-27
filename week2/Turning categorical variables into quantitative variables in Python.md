# Turning categorical variables into quantitative variables in Python

## Categorical variables

**Problem:**

* Most statistical models cannot take in the objects/strings as input

Car | Fuel | ...
--- | --- | ---
A | gas | ...
B | diesel | ...
C | gas | ...
D | gas | ...

**Solution:**

* Add dummy variables for each unique category

* Assign 0 or 1 in each category

Car | Fuel | ... | gas | diesel
--- | --- | --- | --- | ---
A | gas | ... | 1 | 0
B | diesel | ... | 0 | 1
C | gas | ... | 1 | 0
D | gas | ... | 1 | 0

## Dummy variables in Python Pandas

* Use `pandas.get_dummies()` method

* Convert categorical variables to dummy variables (0 or 1)

fule |                      
--- |
gas |
diesel |
gas | 
gas |

```python
pd.get_dummies(df['fuel'])
```
`pd.get_dummies` **method automatically generates a list of numbers, each one corresponding to a particular category of the variable**

| gas | diesel
| --- | ---
| 1 | 0
| 0 | 1
| 1 | 0
| 1 | 0









