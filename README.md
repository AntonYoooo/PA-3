# PA-3-Pandas
This repository involves programming problems that utilizes the Pandas Library. 

## Problems
#### 1. CSV DataFrame Loader and Row Viewing
The main goal for this problem is to load the csv file named cars into data frames using panda, and display the first and last 5 rows of the resulting cars. 

#### 2. Slicing, Subsetting, and Indexing
After successfully loading `cars.csv`, the following instructions should then be executed via utilization of subsetting, slicing, and indexing operations:
- Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7…) of cars.
- Display the row that contains the ‘Model’ of ‘Mazda RX4’.
- How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?
- Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models

## Solutions
The following programs are the solutions to the previously stated problems. 

### 1. Dataframe Loader and Row viewing
```python
import pandas as pd #syntax to access pandas library 

df = pd.read_csv('cars.csv') #load the file cars.csv into dataframes
print("The First five rows are: \n", df.head()) #prints the first 5 rows 
print("\nThe Last five rows are: \n", df.tail()) #prints the last 5 rows 
```
**Output:** 

![image](https://github.com/user-attachments/assets/138ff208-0e1c-417a-ad42-f8fe6fe5b0c1)

