# WEEK 1

*Introduction to Data Visualization Tools*

* For exploratory data analysis
* Communicate data clearly
* Share unbiased representation of data
* *Matplotlib* 
```notebook
%matplotlib inline
import matplotlib.pyplot as plt

plt.plot(5, 5, 'o')
plt.show()
```
* Line plots: A line plot is a type of plot which displays information as a series of data points called ‘markers’ connected by straight line segments.
```
import matplotlib as mpl
import matplotlib.pyplot as plt

year = list(map(str, range(1980, 2014)))

df_canada.loc('Haiti', years].plot(kind = 'line')
plt.title('Immigration from Haiti')
plt.ylabel('Number of immigrants')
plt.xlabel('Years')

plt.show()
```
