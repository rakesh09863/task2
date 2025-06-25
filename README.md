-# task2
--creating table 

create table emp1(
empid number primary key,
ename varchar2(15) not null,
age number DEFAULT 25,
email varchar2(20),
sal number,
comm number);

select * from emp1;

----inserting data

insert into emp1(empid,ename,age,email,sal,comm) values (1,'rakesh',20,'rakesh@gmail.com',1000,null);
insert into emp1(empid,ename,age,email,sal,comm) values (2,'ek',21,'ek@gmail.com',2000,null);
insert into emp1(empid,ename,age,email,sal,comm) values (3,'guru',23,'guru@gmail.com',3000,500);
insert into emp1 values(4,'vignesh','21','vignesh@gmail.com',2000,1000);
insert into emp1(empid,ename,email,sal,comm) values (5,'raju','raju@gmail.com',1000,null);
insert into emp1(empid,ename,email,sal,comm) values (6,'summi','summi@gmail.com',4000,2000);
insert into emp1 values(7,'shilpa','25','shilpa@gmail.com',5000,1000);
insert into emp1 values(8,'gayi','22','gayi@gmail.com',null,2000);
insert into emp1 values(9,'subbu','25','subbu@gmail.com',2000,null);
insert into emp1 values (&empid,&ename,&age,&email,&sal,&comm);

----nvl(),nvl2(),is null,is not null replacing Nulls

select empid,ename,age,email,nvl(sal,500),comm from emp1;
select empid,ename,age,email,sal,nvl(comm,500) from emp1;
select empid,ename,age,email,sal,comm,nvl(sal,sal+comm) from emp1;
select empid,ename,age,email,sal,comm,nvl2(sal,'yes','no') from emp1;
select empid,ename,age,email,sal,comm,nvl2(comm,'yes','no') from emp1;
select empid,ename,age,email,sal,comm from emp1 where comm is null;
select empid,ename,age,email,sal,comm from emp1 where comm is not null;

--------update

select * from emp1;

update emp1 set comm = 100 where ename ='rakesh';
update emp1 set ename = 'd.rakesh' where email ='rakesh@gmail.com';
update emp1 set sal = 5000 where ename ='gayi';
update emp1 set age = 25 where ename ='d.rakesh';
update emp1 set comm = 1000 where ename ='jannu';
update emp1 set ename ='rakesh',age ='21' where empid =1;
update emp1 set ename ='ek',age ='23',email ='krishna@gmail.com' where empid =2;
update emp1 set sal = sal+sal*18/100 where ename ='ek';


---------delete

delete from emp1 where sal is null;
delete from emp1 where ename ='rakesh';
delete from emp1 where comm is null;
delete from emp1 where email ='rakesh@gmail.com';



