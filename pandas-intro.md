# Pandas intro

## Import pandas

```python
import pandas as pd 
```

## Import a CSV file

```python
df = pd.read_csv('file_name.csv') #for comma separated values (default)
df = pd.read_csv('file_name.csv', sep = ';') #for semicolon separated values
df
```

## Print information on data

```python
df.head() # Prints the first 5 rows of the dataset

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
#
# our code to be executed
#
print(time.time() - start, 'seconds')
```

