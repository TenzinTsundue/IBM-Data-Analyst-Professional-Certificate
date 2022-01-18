# WEEK 3
*Exploratory Data Analysis*
* Summarize main characteristics of the data
* Gain better understanding of the data set
* Uncover relationships between variables
* Extract important variables

Descriptive Statistics
* Describe basic features of data
`df.describe()`<br>
`df["column"]value_count()`<br>
* Box Plots
* Scatter Plot

*GroupBy in Python*
```
df_test = df[[‘drive-wheel’, ‘body-style’, ‘price’]]
df_grp = df_test.groupby(['drive-wheels', 'body-style'], as_index=False).men()
df_grp
```
* Pivot()
	* One variable displayed along the columns and the other variable displayed along the rows.
```
df_pivot = df_grp.pivot(index= 'drive-wheels', columns='body-style')
```
* Heatmap
	* Plot target variable over multiple variables
```
plt.pcolor(df_pivot, cmap='RdBu')
plt.colorbar()
plt.show()
```
* Correlation
	* Measures to what extent different variables are interdependent
	* Correlation doesn’t imply causation
* Pearson Correlation
	* Measure the strength of the correlation between two features
		* Correlation coefficient (-1<0<+1): close to 1 or -1
		* P-value (0.1<0.05<0..001): strong when less than 0.001		
* Chai-Square
	* The Chi-square tests a null hypothesis that the variables are independent.
	* The Chi-square does not tell you the type of relationship that exists between both variables; but only that a relationship exists.
