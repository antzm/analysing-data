# Pandas intro

## Import pandas

```python

import pandas as pd 

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

df.head() # Prints the first 5 rows of the dataframe (defult = 5 rows)

df.head(15) # Prints the first 15 rows of the dataframe

df.tail() # Prints the last 5 rows of the dataframe (default = 5 rows)

df.tail(15) # Prints the last 15 rows of the dataframe

df.info() # Prints a summary of the dataframe

df.describe() # Prints decriptive statistics for each column of the dataframe

df.nunique() # Prints the number of unique values in each column

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
