# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.


## DML(Data Manipulation Language)
<div align="justify">
The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.
</div>

## List of DML commands: 
<div align="justify">
INSERT: It is used to insert data into a table.<br>
UPDATE: It is used to update existing data within a table.<br>
DELETE: It is used to delete records from a database table.<br>
</div>

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/af6ae5bb-beb8-437c-a445-117f72bd22f6)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/2d047638-5e7c-4814-9ed6-b327be485766)

### Q2) Delete the records from manager table where the salary less than 2750.
## QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/296f9c03-ced4-4a48-8646-d3724d19fe1c)

## OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/e53ae883-5a37-4c09-989a-e04ab0bec08a)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)
### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/5a78494b-6c6f-4540-a1cf-db6dee09b679)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/8a91abeb-b40f-4fa2-8894-9f9d2775acda)

### Q5)	List the names of Clerks from emp table.
## QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/86c76ff9-07b0-42d6-a958-49fe7a3cd98e)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/c16da6df-5357-4c39-8c70-ab98b16243aa)

### Q6)	List the names of employee who are not Managers.
### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/4c59b591-b195-49da-a7c9-01005efba573)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/3f1089e7-77e8-4be1-9f58-5ffa8ada217f)

### Q7)	List the names of employees not eligible for commission.
### QUERY:
  ![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/9c72d562-ed2a-45ba-b04a-2b9b805dd109)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/2d9dad92-edfb-4c01-8e59-f00b07ac60e1)


### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/a8a76eaa-d6dc-4e73-8fd8-40fcca3d6f65)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/6788b6c9-155a-4f5e-ae01-f1b8ed09ff73)


### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/b6c5cde8-4f1d-43d8-a5b2-449886ab45de)


### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/b3c64705-4b39-4592-9f3f-8169de77c546)


### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/80c7daa2-deaf-4c82-a330-2bdc8fdc080b)


### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/e19daeb8-a044-419e-b3b5-0cf5a1f4156b)


### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/da52a51b-7951-48ce-bc39-8441821b7235)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/0251da19-8156-4df0-80cb-d75078abd353)


### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/a79d1ac7-64ab-4759-93bb-660785cd4ed3)


### OUTPUT:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/1a101c55-e7a1-47ba-bde2-93022a430b24)

### Q13) Find number of rows in the table EMP

### QUERY:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/2e241604-1261-4dba-a1c5-1e9b83b71dc7)

### OUTPUT:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/5cb51408-0599-4e93-b01d-586135250ae4)


### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/f5583cb0-efda-4e61-89d2-0115e636be58)


### OUTPUT:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/e6bc3ecd-97d4-4c1f-89d9-835e1564393d)


### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/137122d4-fc0b-46f2-b42a-cbdd05411804)


### OUTPUT:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/9dd7d0fa-5c72-43ef-8abd-85c6a17d3fb8)
### RESULT:
Thus the Data Manipulation Language (DML) Commands and built in functions in SQL

