![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/e813a978-ec9a-44c0-afe2-f5ccf5cda12f)# EX-3-SubQueries-Views-and-Joins
## DATE:

## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/cd4b580b-9f6e-4523-83a8-8dea6a691a9b)


### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/57845edc-b76e-497a-8462-17b7322598fc)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/970c0f2c-aaf0-4113-9c3c-ff55b22cf548)


### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/e28d8197-d5c6-4145-aba4-b1cf4910352e)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/252ef662-1734-45d9-ad6c-0674ea66e9b2)


### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/0d3c7fb3-7de9-4b84-8473-a470d4e1f155)


### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/b7e1bf4b-beba-4f2f-8946-a89b09f15f75)


### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/b3607024-374c-4476-9216-c215d73770a3)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:

![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/32a91de7-c3b4-4114-bb96-a10d1e2932aa)

### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/f80be858-c474-4770-b5cd-927a8a82085b)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/abd05763-c76e-4b71-9e7e-41d98ab2e694)


### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/4b4ca806-b585-48d0-8332-0b06269b3458)

## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/bbdbc504-57df-466d-bce9-d15a17f80796)


### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/cf4e44e3-5f74-4366-acc3-e55f1725cb1d)

### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/ed8f7179-e6c7-4ced-bd15-96412442f19a)


### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/fc24c629-6796-4919-9835-054b9ac947ec)

### Q9) Perform Natural join on both tables

### QUERY:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/a40d7b1d-c7a5-4a4b-b97f-3bb9e4152ca5)


### OUTPUT:
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/ef01d952-b83e-40ab-9b33-acfb9c499f50)

### Q10) Perform Left and right join on both tables

### QUERY:
   ## Left Join
   ![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/f621c323-8c67-4b85-96fc-9e7d822083ce)


   ## Right join
    ![image](https://github.com/DhanushPalani/EX-3-SubQueries-Views-and-Joins/assets/121594640/8be146f2-c02a-4c31-8dd7-a759a92e69c3)

### OUTPUT:
   ## Left Join
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/200507a4-a464-4bb6-908b-1ed251de645a)


   ## Right Join
![image](https://github.com/vijayarajv1704/EX-3-SubQueries-Views-and-Joins/assets/121303741/57145af7-2124-4d56-a473-13bbd2500a3f)

### RESULT:
Output is sucessfully got.
