# SQL Basics

## SELECT ... FROM ...

Used to select certain columns from the specified table

```SQL
SELECT column1, column5, column8
FROM table3;
```

Using a star (\*) selects all the columns from  the specified table

```SQL
SELECT *
FROM table1;
```

## LIMIT

Used at the end of the SQL statemnt to limit the number of the displayed results.

```SQL
SELECT column1, column5, column8
FROM table3
LIMIT 100;
```

## ORDER BY

Used to order (short) results according to a certain column or columns.

```SQL
SELECT column1, column5, column8
FROM table3
ORDER BY column5
LIMIT 25;
```

Placing `DESC` after the column name, the results are ordered (shorted) in descenting order. Otherwise, results are always shorted in ascending order.

```SQL
SELECT column1, column5, column8
FROM table3
ORDER BY column5 DESC;

SELECT column1, column5, column8
FROM table3
ORDER BY column5 DESC, column1;

SELECT column1, column5, column8
FROM table3
ORDER BY column5 DESC, column1, column8 DESC;

```

## WHERE

The `WHERE` statement is used for filtering the data and thus, it dispalys only the subsets of the data that meet ceertain criteria.

```SQL
SELECT column1, column5
FROM table8
WHERE column1 <= 50
```

## Operators

### Comparison Operators


Comparison Operator | Meaning
--------------------|--------
\= | equal to
\!= | not equal to
\> | greater than
\< | less than
\>= | greater than or equal to
\<= | less than or equal to


### Arithmetic Operators

Arithmetic Operators| Meaning
--------------------|-------
\+ | Addition
\- | Subtraction
\* | Multiplication
\/ | Division

