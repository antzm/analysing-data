# Pandas intro

## Import pandas

```python

import pandas as pd 

```

## Creating a Pandas Series
```python

pet_ages = pd.Series(data = [3, 8, 1, 1], index = ['cat', 'dog', 'hamster', 'fish'])

# or 
pet_ages = pd.Series([3, 8, 1, 1], ['cat', 'dog', 'hamster', 'fish'])

# Checking if an idex exists
check_dog = 'dog' in pet_ages
print(check_dog)
# True



```

## Accessing a Pandas Series
```python
pet_ages
# cat 3 
# dog 8
# hamster 1
# fish 1

pet_ages['dog']
# 8

pet_ages[['dog', 'fish']]
# dog 8
# fish 1

pet_ages[0]
# cat 3

pet_ages[[1, 3]]
# dog 8
# fish 1

pet_ages[-1]
# fish 1

```

## Making changes and calculations to a Panda Series
```python
# Changing the Dog's age
pet_ages['dog'] = 12
pet_ages['dog']
# dog 12

# Adding 2 to the Dog's age
pet_ages['dog'] = pet_ages['dog'] + 2
pet_ages['dog']
# dog 14

# Only print the ages plus 1
print(pet_agess + 1)
# cat 4
# dog 9
# hamster 2
# fish 2

# Boolean select certain ages
older_pets = pet_ages[pet_ages > 2]
older_pets
# cat 4
# dog 9

```

## Creating Pandas DataFrames

```python
# Creating DataFrame from a dictionary of Pandas Series 
stat_info = {'Country 1' : pd.Series(data = [245, 25, 55], index = ['var1', 'var5', 'var8']),
             'Country 2' : pd.Series(data = [40, 110, 500, 45], index = ['var5', 'var7', 'var8', 'var15'])}

df = pd.stat_info
```



## Import a CSV file and save a CSV file

```python

df = pd.read_csv('file_name.csv') # Imports a CSV with comma separated values (default = comma)
df = pd.read_csv('file_name.csv', sep = ';') # Imports a CSV file with semicolon separated values

df.to_csv('file_name.csv') # Saves the dataframe as file_name.csv
df.to_csv('file_name.csv', index = False) # Saves the dataframe as file_name.csv without the index

```

## Print information about a dataframe

```python

df # Prints the dataframe

df.head() # Prints the first 5 rows of the dataframe (defult = 5 rows)

df.head(15) # Prints the first 15 rows of the dataframe

df.tail() # Prints the last 5 rows of the dataframe (default = 5 rows)

df.tail(15) # Prints the last 15 rows of the dataframe

df.sample(10) # Prints 10 random lines of the dataaframe, i.e. not sequensial

df[['column_1,', 'column_8', 'column_15']] # Prints only the selected columns

df.column_3 # Prints only the slected column, i.e. it returns a series
#or
df['column_3'] # Prints only the slected column, i.e. it returns a series

df.info() # Prints a summary of the dataframe

df.describe() # Prints decriptive statistics for each column of the dataframe

df.nunique() # Prints the number of unique values in each column

```

## Filtering values

```python

df[df.column_5 == 'my_value'] # Returns only the rows of the dataset that have the value 'my_value' in column_5
df[df.column_2 > 'my_value'] # Returns only the rows of the dataset where column_2 is greater than 'my_value'
df[df.column_1 >= 'my_value'] # Returns only the rows of the dataset where column_1 is greater than or equal to 'my_value'
df[df.column_8 < 'my_value'] # Returns only the rows of the dataset where column_8 is less than 'my_value'
df[df.column_3 <= 'my_value'] # Returns only the rows of the dataset where column_3 is less than or equal to 'my_value'

```


## Calculate the mean of a column

```python

column_mean = df['column_name'].mean()

```

## Replace the missing values in a column with the column mean
```python

df['column_name'] = df['column_name'].fillna(column_mean)

# or

df['column_name'].fillna(column_mean, inplace=True)

```

# Additional info

## Counting the time that it takes for our code to be executed

```python

import time
start = time.time()

# code to be executed

print(time.time() - start, 'seconds')

```
