# EX-3-SubQueries-Views-and-Joins

# DATE:

# AIM:  To make an experient on the SubQueries , Views and Joins.
      
        

        
# Create employee Table

```
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```

# Insert the values
```
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



# Create department table


```

CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));

```


# Insert the values in the department table



```
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');

```
# Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.

# QUERY:

<img width="625" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/4da768df-84f3-4a8c-85aa-1e184b5d672c">


# OUTPUT:

<img width="142" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/b8622f9f-3faf-4218-a971-832c0028ca68">


# Q2) List the ename,job,sal of the employee who get minimum salary in the company.

# QUERY:

<img width="578" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/e9647973-af79-4a1e-a179-7b284c225d0b">

# OTUPUT:

<img width="317" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/6235cc68-e4dd-4965-a696-d94b63b9adfa">


# Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

# QUERY:


<img width="634" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/af237eb7-efb2-4a04-8e0b-d6b8997ce0da">


# OUTPUT:

<img width="163" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/70e7db53-9cee-417f-b12c-32e3d1438b92">


# Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

# QUERY:

<img width="628" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/4d60f20e-18a0-432a-abfd-0da8334b07e9">

# OUTPUT:


<img width="141" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/2cc9bbed-e2a9-4566-bf70-fb71e626da08">



# Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.


# QUERY:


<img width="631" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/0210d44a-5c6d-4ff6-a2b3-9f0ef1be5cf3">



# OUTPUT:


<img width="377" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/d792f018-fd12-4b38-a976-23eec0c0d416">




# Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table


# QUERY:


<img width="547" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/da284c6e-6627-4237-a92a-69e5d8fdc09f">



# OUTPUT:


<img width="376" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/f5cd1cff-d99e-441e-9c6f-a4b468552a41">



# Create a Customer1 Table


CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);


# Inserting Values to the Table

```
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```

# Create a Salesperson1 table
```
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
# Inserting Values to the Table

```
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```

# Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

# QUERY:


<img width="637" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/c452ad5c-1a03-4b96-acc6-9262689b0174">


# OUTPUT:


<img width="570" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/307dd60f-ef3c-400a-b8b1-ee64b7ed2c29">




# Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


# QUERY:

<img width="638" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/2c628085-5574-43fc-8864-3d4752eb3663">


# OUTPUT:


<img width="629" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/87e9b5f0-3ea2-439f-af92-c2e5833c9e20">



# Q9) Perform Natural join on both tables


# QUERY:

<img width="637" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/1c7bdf18-bebd-47be-93a8-83e026886801">


# OUTPUT:

<img width="637" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/5a33d1e3-333d-4d16-8d72-cf9243281678">



# Q10) Perform Left and right join on both tables


# Left Join

<img width="641" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/64237bb4-9958-4b21-a861-6bb8c7d8a4fd">


# Right Join 

<img width="633" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/528f7953-1c7e-4b89-aece-b91a21752781">


# OUTPUT:


# Left Join 


<img width="631" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/c6736840-cc86-42ea-9b1c-3b0004d8bc02">

# Right Join


<img width="599" alt="image" src="https://github.com/AlluguriSrikrishnateja/EX-3-SubQueries-Views-and-Joins/assets/118343892/290ef10d-70af-44a8-9654-8c96ed4e0cc5">





































































