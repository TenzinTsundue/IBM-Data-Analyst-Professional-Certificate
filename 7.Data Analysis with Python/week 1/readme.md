# WEEK 1
*Importing Datasets*
* Python Package for DataScience
	* Scientifics Computing (eg. Pandas, NumPy, SciPy)
	* Visualization(eg. Matplotlib, Seaborn)
	* Algorithmic(eg. Sickest-learn, Statsmodels)
* Importing and Exporting Data in Pyhton
```
import pandas as pd
url = "https://filepath.data"
df = pd.read_csv(url, header=None)
```
* Analyzing data with python
	* Data Types `df.dtypes`
	* Data Distribution `df.describe()
	* `df.info()`
* Accessing databases using Python
	* SQL API
```
CONNECT(df,user,pswd)
SEWND("update employee set..")
EXECUTE()
STATUS_CHECK()
OK
DISCONNECT()
```
	* DB-API
		* Connection Objects
			* Database connections
			* Manage transactions
		* Cursor Objects
			* Database Queries
```
from dbmodule import connect

#Create connection object
connection = connect('databasename','username','pswd')

#Create a cursor object
cursor = connection.cursor()

#Run queries
cursor.execute('select * from mytable')
results = cursor.fetchall()

#Free resources
Cursor.close()
connection.close()
``` 
