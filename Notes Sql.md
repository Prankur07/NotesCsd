# ANSI SQL using MySQL

>ANSI SQL: Structured Query Language
This is a 5th gen language used to interact or 
communicate with the DMBS software..

### What is DBMS? 
Database Management System Software
which will help me to store, arrange and manage this
data. It should also have features like providing
security and also take backup and retrive back the data
(in case of some unavoidable circumstances). 

    Oracle Corp: Oracle 19c, MySql
    Microsoft: SQL Server

### What is database?
 A db. is a logical collection
of related information.
    
    roll|name|dob|stream|sem|cgpa|mobile|email|12th%|10th%

### ANSI tried to standardize SQL such that the commands 
are 80% common across DBMSs.
SQL 

    a) DDL: Data Definition
    - create, alter, drop and truncate
    b) DML: Data Manipulation
    - insert, update and delete
    c) DQL: Data Query
    - select and its sub clauses
    d) DCL: Data Control
    - grant and revoke
    e) TCL: Transaction Control
    - commit, rollback and savepoint

TRANSACTION

    withdraw money
    insert statement in the transaction table
    accountno|where|amount|date|time
    1234|ATM-1|3000|29-06-2021|10:54:00
    update statement on the accounts table
    accountno|accholdername|balance
    1234|Sumita|53000

>Backup Process: Every Friday the DBA schedules
a backup of the entire db at 19:00:00.
 
### DDL:
>create a db object like a table, view, etc..

>A table(aka relation) is a collection of rows and 
columns.

>The name,model, brand are nothing but the fields
of a table trainee, car, laptop resp.

### ER diagram

+ Trainee,Laptop,Car are called ENTITIES [represented by
rectangle boxes].
+ The fields are known as attributes (columns)[represented
by ellipses]. 

    * TRAINEE HAS A LAPTOP
    * TRAINEE OWNS A CAR

+ Two entities can be related to each other.
[represented by diamond]

    + trainee
        * name
        * dob
        * mobile
        * email
        * pct_12

    * laptop
        + processor
        + brand
        + warranty
        + ram/hdd
        + price
        + os
        + weight
    * car
        + model
        + company
        + engine(cc)
        + mileage
        + color
        + features
        + fuletype

## What is a constraint? 
Constraint is a rule
to be applied on the columns of a table to 
ensure data integrity.

###  primary key:
>A column or a group of columns
which helps us to uniquely identify a record from 
others. Generally, chosen as a pseudo column.

* Trainee: rollNo
* Laptop: laptopId
* Car: carNo

    Such a column cannot be left empty/blank/null
    Even it cannot have any duplicate values.
        **PK=UNQ+NN**

A table can have only one PK but multiple UNQ constraints
is possible.

### unique constraint:
    Such a column cannot
    have duplicate values but can be null once.
### check constraint:
    A column is allowed to have 
    values from a pool(aka domain).

* Boiler
    * boiler_id
    * boiler_name
    * location
    * content
    * temp numeric [200-5000]

### foreign key constraint:

Such a column refers
to another column of the same or different table.
If you have applied such a constraint:

    a) you cannot insert a record(row) into the table
    if there is no matching value present in the referred
    table.

    b) you cannot delete a record from the referred table
    if there are matching records present in the 
    dependent table.

>Trainee has a laptop,
In the LAPTOP table, we will keep a column called
trainee_id[FK] that will refer to id [PK] column of 
the TRAINEE table.

### Lets start off with a demo....
```sql
-- create a new db
create database csd;
--Query OK, 1 row affected (0.06 sec)
use csd
--Database changed
select database();

-- +------------+
-- | database() |
-- +------------+
-- | csd        |
-- +------------+
-- 1 row in set (0.00 sec)

create table trainee(
id int primary key,
name varchar(50) not null,
gender char(1) not null,
dob date,
mobile varchar(10) not null,
email varchar(50)
);
-- to check the strucure of the table
describe trainee;
```

### The data types:
 * int 
 * bigint 
 * bit [0,1],
 * char
 * varchar
 * date
 * blob [images]
```sql
create table laptop(
id int primary key,
modelNo varchar(20) not null,
manufac varchar(20),
owner_id int not null,
foreign key(owner_id) references trainee(id)
);
```

### DML commands:
    
    insert, update, delete
```sql    
insert into trainee
values(1,'Samuel','M','2002-05-18','123456','sam@xyz.com');
insert into trainee
values(2,'Samuel','M','2002-05-18','123741',null);
-- multiple row insert (mysql)
insert into trainee
values
(3,'Karan','M','2002-11-18','156423','karan@xyz.com'),
(4,'Preeta','F',null,'156742','preeta@xyz.com'),
(8,'Arvind','M','2002-11-28','693852','arvind@xyz.com');
-- to see the records present in trainee table
select * from trainee;
```

```sql

-- to see structure of the table trainee
desc trainee;

-- alter the table to change the size of a column
alter table trainee
modify email varchar(100);

-- alter the table to add new column with a default value
alter table trainee
add city varchar(50) default 'pune';

-- alter tha table to rename a column (mysql)
alter table trainee
change id tid int;

-- insert a record into child table
insert into laptop
values(105,'LN1564',null,4);

-- the below one fails as no trainee with tid=45
insert into laptop
values(105,'LN1564',null,45);

-- the below query fails as there are dependent
-- records present in the laptop table
delete from trainee
where tid=4;

-- the below query succeds as there is no dependent
--record in the laptop table for tid=1
delete from trainee
where tid=1;
```