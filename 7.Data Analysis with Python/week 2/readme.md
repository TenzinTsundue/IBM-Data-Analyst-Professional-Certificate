# WEEK 2
*Data Wrangling*
*Data Pre-processing*
> The process of converting or mapping data from the initial “raw” form into another format, in order to prepare the data for further analysis.

1. Identify and handle missing value 
	*  Drop the missing values (variable or data entry)
	* Replace the missing values (average or frequency or based on other function)
	* leave it as missing data
```
#drop null
df.droopna(subset=["price"], axis=0, inplace = True)

#replace value
df["normalized-losses"].replace(np.nan, mean)
```

2. Data Formatiing
	* Data are usually collected from different places and stored in different formats.
	* Bringing data into a common standard of expression allows to make meaningful comparison.
```
df.rename(columns={”city_mpg”: “city-L/100km”}, inplace=True)
```
3. Data Normalization(entering/scaling)
	* Simple Feature scaling (0-1)
	* Min-Max
	* Z-score
4. Data Binning
	* Binning: Grouping of values into “bins”
	* Converts numeric into categorical variables
	* Group a set of numerical values into a set of “bins”
5. Turning Categorical values to numeric variables
	* Use pandas.get_dummies() method
```
pd.get_dummies(df['fuel'])
```
