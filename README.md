# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 16-02-2024

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
### Population:
~~~
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2015"].mean()
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()
~~~
### Market Price:
~~~
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
~~~
### Temperature:
~~~
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
~~~
# OUTPUT:
### Population:
![](https://github.com/RanjithD18/TSA_EXP1/blob/main/1.png)
### Market Price:
![](https://github.com/RanjithD18/TSA_EXP1/blob/main/2.png)
![](https://github.com/RanjithD18/TSA_EXP1/blob/main/3.png)
### Temperature:
![](https://github.com/RanjithD18/TSA_EXP1/blob/main/4.png)





# RESULT:
Thus we have created the python code for plotting the time series of given data.
