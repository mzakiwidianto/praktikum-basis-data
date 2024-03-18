# **MODULE 2**

## A. INTRODUCTION DATA MANIPULATION LANGUAGE


## B. COMMANDS IN DATA MANIPULATION LANGUAGE 
### 1. SELECT
### 2. INSERT
### 3. UPDATE
### 4. DELETE

## C. LOGIC OPERATORS
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

## E. ARITHMETIC OPERATORS
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

## G. SUBQUERY
A subquery, also known as a nested query or subselect, is a form of query embedded within another query using the SELECT, WHERE, or FROM clauses. The purpose of a subquery is to generate data that will be used in the main query to limit or filter the data to be retrieved. Subqueries are used to provide additional conditions or criteria in the data retrieval process. Here are some rules for using subqueries:


Subqueries must be enclosed in parentheses.
- The use of the ORDER BY clause is not allowed in subqueries. The ORDER BY clause can be used in the main SELECT statement.
- The SELECT clause in a subquery must contain a single column name or expression, except for subqueries using the EXISTS keyword.
- By default, column names in a subquery refer to the table names in the FROM clause of the main query by qualifying the column names.
- Subqueries cannot be used as operands in expressions.

```sql
SELECT column_name
FROM table_name
WHERE column_name operator
      (SELECT column_name
      FROM table_name
      WHERE column_name operator);
```
Here is an example of using a subquery:


The database "data_mahasiswa" consists of three tables: mahasiswa, nilai_mahasiswa, and mata_kuliah.
<p align="center">
<img src="img_basdat/01Tabel_Mahasiswa.png" width="310">
      <img src="img_basdat/02Tabel_Nilai.png" width ="310">
      <img src="img_basdat/03Tabel_MK.png" width = "310">
</p>

```sql
SELECT nama
FROM mahasiswa
WHERE nim IN
      (SELECT nim_mahasiswa
       FROM nilai_mahasiswa
       WHERE nilai > 80 AND kode_mata_kuliah = 'mk001');
```

This query is employed to retrieve the names of students from the "mahasiswa" table who meet specific conditions. The embedded subquery serves the purpose of finding student IDs from the "nilai_mahasiswa" table with grades exceeding 80 and associated with the course code “mk001”. The outcome of this subquery, which comprises the qualifying student IDs, is then used as criteria in the main query. Using the WHERE clause and the IN operator, the main query extracts the names of students whose student IDs match the results of the subquery. Therefore, the final result of this query is a list of student names who fulfill the criteria of having a grade above 80 in the course “mk001”.

<p align="center">
<img src="img_basdat/04Hasil_Subquery.png" width="100">
</p>

## H. COMPARISON OPERATORS
### 1. Wildcard
Wildcard is a special character used in search or data filtering operations. Wildcards allow users to match specific patterns within data values, providing additional flexibility in query or search conditions.
<br>

| Symbol        | Usage    | Example      |
| :------------- |:-------------| :-------------|
| %      | Represents zero, one, or more characters |‘baju%’ will find ‘bajubiru’, ‘bajumerah’|
| _      | Represents a single character |‘p_t’ will find ‘pat’, ‘pet’, ‘pit’, ‘pot’, ‘put’|
| [ ]      | Represents any single character within square brackets |‘p[ao]t’ will find ‘pat’ and ‘pot’|
| ^      | Represents any character not in square brackets |‘p[^ao]t’ will find pet’, ‘pit’, ‘put’, but not ‘pat’ and ‘pot’|
| -      | Represents a range of characters |c[a-d] will find cat, cbt, cct, and cdt|.

```sql
SELECT * FROM table_name WHERE column_name LIKE 'baju%'; will show rows that have column values starting with "baju."
```














