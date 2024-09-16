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
- Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.

## Solutions
The following programs are the solutions to the previously stated problems. 

### 1. Dataframe Loader and Row viewing
```python
import pandas as pd #syntax to access pandas library 

df = pd.read_csv('cars.csv') #loads the CSV file "cars.csv" into a dataframe
print("The First five rows are: \n", df.head()) #prints the first 5 rows of the dataframe
print("\nThe Last five rows are: \n", df.tail()) #prints the last 5 rows of the dataframe
```
**Output:** 


![image](https://github.com/user-attachments/assets/5e779d79-ce55-4697-9cdb-7cf69efdd72d)

### 2.a. Odd-numbered columns 
```python
#selects the first 5 rows of the dataframe
#specifically skips every 2 columns, starting from index 0 
odd_columns = df.iloc[:5,::2] 
odd_columns #prints the odd columns 
```
**Output:** 


![image](https://github.com/user-attachments/assets/cf85ac7d-18d5-4a7d-b595-c4e17e65bb2a)

### 2.b. Mazda RX4
```python
df.loc[df['Model']=='Mazda RX4'] #Filters and prints the row where its column is 'Mazda RX4'
```
**Output:** 


![image](https://github.com/user-attachments/assets/63a0ad3b-e608-45d0-8e07-808103442491)

### 2.c. Camaro Z28 Cyl
```python
df.loc[df['Model']=='Camaro Z28', ['Model', 'cyl']] #Filters and prints the 'Model' and 'cyl' columns for the row were 'Model' is 'Camaro Z28'
```
**Output:** 


![image](https://github.com/user-attachments/assets/377f097c-fb54-48d0-8cba-d3fce9395a37)

### 2.d. Cylinders and Gear Types 
```python
df.loc[df['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']), ['Model', 'cyl', 'gear']] #Filters and prints the columns 'Model', 'cyl', and 'gear' of the specified cars 
```
**Output:** 


![image](https://github.com/user-attachments/assets/1903164d-048b-4cdb-a867-50f3bf061e64)


