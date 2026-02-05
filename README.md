Task 2 : Data Insertion and Handling Nulls 
 
we want to create table first by using create command"create table table_name(name datatype);"

--table: emp1
create table table_name(.....);

---Data Insertion using "inset into table table_name"
INSERT INTO emp1 values (.......);
INSERT INTO emp1(.......) VALUES (....);
INSERT INTO emp1 values(&.., &.., &...);

---Handling NULLs
NVL(expr1, expr2) -- Replaces NULL with a default.

NVL2(expr1, yes, no)-- Conditional output based on NULL.

(IS NULL ,IS NOT NULL)   filter records based on NULL values.

-Update
UPDATE emp1 SET column1 = --- WHERE column2 = --;(varchar2() then use ' ')

---Delete
DELETE FROM emp1 WHERE column IS NULL;(remove the null columns)
DELETE FROM emp1 WHERE column = -----;



Key Concepts
------------
Table creation with constraints (PRIMARY KEY, NOT NULL, DEFAULT)

Null value management using NVL, NVL2

Conditional queries(where) using IS NULL, IS NOT NULL

Data updates and conditional salary increment

Data deletion based on logical conditions




