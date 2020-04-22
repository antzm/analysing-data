# Pandas intro

## Import pandas

```python
import pandas as pd 
```

## Import a CSV file

```python
df = pd.read_csv('file_name.csv')
df
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


