# ANOVA

* Why do we perform ANOVA?

  * Finding correlation between different groups of a categorical variable
  
* What we obtain from ANOVA?

  * F-test score: variation between sample group means divided by variation within sample group
  
  * P-value: confidence degree
  
## Example

* ANOVA between 'Honda' and 'Subaru'

```python
df_anova = df[['make', 'price']]
grouped_anova = df_anova.groupby(['make'])
anova_results_1 = stats.f_oneway(grouped_anova.get_group('honda')['price'], grouped_anova.get_group('subaru')['price'])
ANOVA results: F=0.197
				p = F_onewayResult(statistic = 0.19744)
				  =0.6609
```
