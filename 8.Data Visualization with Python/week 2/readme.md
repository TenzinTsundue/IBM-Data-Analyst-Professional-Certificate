# WEEK 2
# Basic and Specialized Visualization Tools
* *Area Plot*
	*  Also known as area chart or area graph
	* Commonly used to represent cumulated totals using numbers or percentages over time.
```
import matplotlib as mpl
import matplotlib.pyplot as plt

df_top5.plot(kind='area')

plt.title('Immigration trend of top 5 Countries')
plt.ylabel('Number of immigrants')
plt.xlabel('Years')

plt.show()
```
* Histogram 
	* A histogram is a way of representing the frequency distribution of a variable.
* Bar Chart
	* A bar chart is commonly used to compare the values of variable at a. Given point in time.
* Pie Chart
```
df_continents('Total').plt(kind='pie')
plt.title('Immigration to Canada by Continent[1980-2013]')
plt.show() 
```
* Box Plot
	* Minimum - First Quartile - Median - Third Quartile - Maximum - Outliers
	* Inter Quartile Range (IQR) : Difference between first and third quartile
* Scatter Plot
```
df_total.plot(
	kind='scatter',
	x='year',
	y='total'
)
```
