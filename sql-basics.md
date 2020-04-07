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
