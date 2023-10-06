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
insert into manager values(7369,'augus',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'leann',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'yogi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'aadhi',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/af6ae5bb-beb8-437c-a445-117f72bd22f6)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/f4005572-31cc-437c-88c9-428690da8f83)


### Q2) Delete the records from manager table where the salary less than 2750.
## QUERY:
```
 delete from manager
 where salary<2750;
```

## OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/b8654e8d-063e-4b30-a321-7162a39d6dbf)


### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)
### QUERY:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/5a78494b-6c6f-4540-a1cf-db6dee09b679)

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/9d2f520b-007a-471e-93d6-8423828bd5b7)


### Q5)	List the names of Clerks from emp table.
## QUERY:
```
select ename from manager where designation='clerk';
```
### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/a1ddc220-47c1-40d4-befd-94deb9643d7f)


### Q6)	List the names of employee who are not Managers.
### QUERY:
```
select ename from manager where designation <> 'manager';
```

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/0df52c16-402b-4b94-aff0-ac49222868cc)

### Q7)	List the names of employees not eligible for commission.
### QUERY:
```
select ename from manager where commission=0;
```
### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/411004d1-b989-47de-9989-674eb4d4cad4)


### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
```
select ename from manager where ename like '%s' or ename like 's%';
```

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/a7788e72-b950-44d0-8677-ea69035a5356)



### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
```
 select ename,designation as "job",deptno,hiredate from manager order by hiredate asc;
```

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/8739bf81-fb08-49a1-9a69-8ce71148a90c)


### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
```
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');
```


### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/f4ea63b2-af15-417d-9a0c-3ae67ecf04c4)


### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
```
select ename,deptno,salary from manager order by deptno asc,salary desc;
```

### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/d59f3188-49d3-43c2-a057-79106d8b5eb9)



### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
```
select ename from manager where deptno not in (30,40,10);
```


### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/d07cea86-c192-4819-a4f3-0f82f9daac62)


### Q13) Find number of rows in the table EMP

### QUERY:
```
select count(*) from manager;
```

### OUTPUT:

![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/6af1a706-ce15-4eed-a880-96edd77397ae)



### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:
```
select max(salary) from manager;
select min(salary) from manager;
select avg(salary) from manager;
```
### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/51e9f0b1-9be6-4959-912a-881549e40cff)


### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:

```
 SELECT designation AS job, COUNT(*) AS num_employees FROM manager GROUP BY designation ORDER BY num_employees DESC;
```


### OUTPUT:
![image](https://github.com/Augustine0306/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119404460/f524970c-f9f2-4ef0-a429-2bd43aa4f549)

### RESULT:
Thus the Data Manipulation Language (DML) Commands and built in functions in SQL

