SQL


---
Terminology
Table
Row
Column (Field / Attribute)
Tuple
Cardinal


---
Keys 
Primary
Unique
Foreign
Candidate
Composite
Primary Key Properties
Primary vs Unique
Primary vs Foreign
Is Foreign Key Always a Primary Key of another Table ?

---

---
Sorting ASC vs DESC
DESCRIBE : DESC
DISTINCT
LIMIT & OFFSET

---

Pattern Matching
LIKE
RLIKE
REGEX_EXP
WildCard
%,_


---
NULL
IS NULL
IS NOT NULL

---

Relationships
One to One
One to Many
Many to One
Many to Many


Union vs UnionAll

Where vs Having

---
Normalization
1NF
2NF
3NF
BCNF
4NF
5NF

Denormalization
ACID


COMMIT / ROLLBACK / SAVEPOINT
Window Function : ROW_NUMBER vs RANK vs DENSE_RANK
Procedure
View

---

Index
Clustered Index
Non-Clustered Index

CONCAT vs CONCAT_WS
IN

Delete / Truncate / Drop

---
- https://www.youtube.com/playlist?list=PLGf6Ram2AQh2GpckMjstVH6AaTm0kPfgI



--- 
Database

Database 

create database test_db;
Show databases;
use sql_pratice_2026;
show tables;
delete database test_db; // Invalid Command
drop database test_db;


---



Joins

1. Inner Join
   1. Equi Join
   2. Non-Equi Join
2. Outer Join
   1. Left Outer Join (Left Join)
   2. Right Outer Join (Right Join)
   3. Full Outer Join
3. Cross Join
4. Self Join
   1. Self Inner Join
   2. Self Left Join
   3. Self Right Join


Rule of thumb for interviews
INNER JOIN → "Only matching records."
LEFT JOIN → "Keep all records from the left table."
RIGHT JOIN → "Keep all records from the right table."
FULL OUTER JOIN → "Keep all records from both tables."
CROSS JOIN → "Generate every possible combination."
SELF JOIN → "Relate rows within the same table, such as employee–manager or parent–child relationships."


Joins Example 
Employee and Department

Employee : Left
Department : Right

Inner : Show Only employee that belongs to department

Left  : Show All employee , If employee has department show it
otherwise department columns are null

Right : Show All department , If department has employee show it
Otherwise employee columns are null

Cross : Show all employee and all department
Self :  Join employee with employee

---