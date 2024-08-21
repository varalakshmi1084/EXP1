# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data(Date,Gold Price)
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt

### Load the dataset
data = pd.read_csv("/content/Gold Price.csv")

### Convert the 'Date' column to datetime
data['Date'] = pd.to_datetime(data['Date'])

### Plotting the 'Price' column over time
plt.figure(figsize=(10,6))
plt.plot(data['Date'], data['Price'], label='Gold Price', color='gold')

### Adding title and labels
plt.title('Gold Price Over Time')
plt.xlabel('Date')
plt.ylabel('Price (INR)')

### Displaying the plot
plt.legend()
plt.grid(True)
plt.show()
```
# OUTPUT:
![EX-01A](https://github.com/user-attachments/assets/a55625f2-37c3-4c0a-8e3e-8b9d283a5d13)
# RESULT:
Thus we have created the python code for plotting the time series of given data.
