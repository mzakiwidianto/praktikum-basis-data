# **MODULE 2**

## A. PENGENALAN DATA MANIPULATION LANGUAGE


## B. PERINTAH PADA DATA MANIPULATION LANGUAGE 
### 1. SELECT
### 2. INSERT
### 3. UPDATE
### 4. DELETE

## C. OPERATOR LOGIKA
### 1. AND
### 2. IN 
### 3. OR
### 4. NOT 
### 5. LIKE

## D. SET OPERATIONS
### 1. UNION (∪)
UNION is an operator that returns values from two or more tables by combining SELECT statements without returning duplicate values. 
There are several rules for using UNION, such as the columns in the combined tables must have the same number and data types, and the order of columns in the combined tables must also be the same.

```sql
SELECT column-1, column-2, ..., column-n
FROM table_name
WHERE condition

UNION

SELECT column-1, column-2, ..., column-n
FROM table_name
WHERE condition;
```

<p align="center">
<img src="img_basdat/union.png">
</p>

UNION ALL is an operator that returns values from two or more tables by combining SELECT statements while returning its duplicate values. 
The difference between UNION and UNION ALL lies in the returning of values; UNION doesn't return its duplicate values, whereas UNION ALL does.

```sql
SELECT column-1, column-2, ..., column-n
FROM table_name
WHERE condition

UNION ALL

SELECT column-1, column-2, ..., column-n
FROM table_name
WHERE condition;
```

<p align="center">
<img src="img_basdat/union%20all.png">
</p>

### 2. INTERSECT (∩)
INTERSECT is an operator that takes the intersection of two SELECT statements.

```sql
SELECT column-1, column-2, ..., column-n
FROM table_name
WHERE column_name IN(
SELECT column-1, column-2, ..., column-n
FROM table_name);
```
<p align="center">
<img src="img_basdat/intersect.png">
</p>

### 3. EXCEPT (-)
EXCEPT is an operator that only returns unique or exclusive data from the first table but not found in the second table. The term "unique or exclusive data" refers to data that has no equivalent in the second table.

```sql
SELECT column-1, column-2, ..., column-n
FROM table_name
WHERE column_name NOT IN(
SELECT column-1, column-2, ..., column-n
FROM table_name);
```
<p align="center">
<img src="img_basdat/except.png">
</p>

## E. ARITHMETIC OPERATIONS
Arithmetic Operators in SQL are used to perform simple arithmetic operations such as addition (+), subtraction (-), multiplication (*), division (/), and modulus (%).
### 1. Addition (+)
Addition is used to add two values.
```sql
SELECT column1, column2, column2 + number FROM table_name;
```
<p align="center">
<img src="img_basdat/penjumlahan.png">
</p>

### 2. Subtraction (-) 
Subtraction is used to subtract one value from another.
```sql
SELECT column1, column2, column2 - number FROM name_table;
```
<p align="center">
<img src="img_basdat/pengurangan.png">
</p>

### 3. Multiplication (*)
Multiplication is used to multiply two values.
```sql
SELECT column1, column2, column2 * number FROM table_name;
```
<p align="center">
<img src="img_basdat/perkalian.png">
</p>


### 4. Division (/)
Division is used to divide one value with another value.
```sql
SELECT column1, column2, column2 / number FROM name_table;
```
<p align="center">
<img src="img_basdat/pembagian.png">
</p>

### 5. Modulus (%)
Modulus is used to obtain the remainder of the division operation between two values.
```sql
SELECT column1, column2, column2 % number FROM table_name;
```
<p align="center">
<img src="img_basdat/modulus.png">
</p>

## F. AGGREGATE OPERATORS
Aggregate operators, commonly known as aggregate functions, are operators used to summarize data within a table. These operators can be used in various DML statements, such as SELECT, GROUP BY, etc.
### 1. SUM
SUM is used to calculate the total value within a column.
```sql
SELECT SUM(column_name) FROM table_name;
```
<p align="center">
<img src="img_basdat/sum.png">
</p>

### 2. AVG
AVG is used to calculate the average value within a column.
```sql
SELECT AVG(column_name) FROM table_name;
```
<p align="center">
<img src="img_basdat/avg.png">
</p>


### 3. MIN
MIN is used to find the minimum value in a column.
```sql
SELECT MIN(column_name) FROM table_name;
```
<p align="center">
<img src="img_basdat/min.png">
</p>


### 4. MAX
MAX is used to find the maximum value in a column.
```sql
SELECT MAX(column_name) FROM table_name;
```
<p align="center">
<img src="img_basdat/max.png">
</p>


### 5. COUNT
COUNT is used to count the number of rows in a table.
```sql
SELECT COUNT(column_name) FROM table_name;
```
<p align="center">
<img src="img_basdat/count.png">
</p>










