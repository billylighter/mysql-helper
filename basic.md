# 💾 MySQL Basics

---

### 🔑 Authorization:

*   #### Login
    > *mysql -u login -p;*

>

---

### 🔑 Basic commands:

* #### Show all databases
  > *SHOW databases;*
  
* #### Create database
  > CREATE database database_sample;

* #### Remove database
  > *DROP database database_sample;*

* #### Select database
  > *USE database_sample;*

---

### 🔑 Table commands:

* #### Show all tables
  > *show tables;*

* #### Create table
  > *create table teacher(
  id INT auto_increment primary key, title varchar(255) not null
  );*

* #### Create connected table by field
  > *create table lesson(
  id INT auto_increment primary key, name varchar(255) not null, teacher_id int not null, foreign key (teacher_id) references teacher(id)
  );*

* #### Remove table
  > *drop table teacher;*

* #### Show table columns
  > *show columns from table_name;*

* #### Insert data to table
  > *insert into teacher (surname) values ('Bondarenko');*

* #### Get all data from the table
  > *select * from teacher;*

* #### Get certain field from the table
  > *select id from teacher;*

* #### Get more than 1 field from the table
  > *select id, surname from teacher;*

* #### Get unique rows which not have same values from the table
  > *select distinct surname from teacher;*

* #### Get row by field from the table
  > *select * from teacher where id = 1;*

* #### Get rows by field with restricted count from the table
  > *select * from teacher limit 3;*

* #### Get rows by field with restricted count from the table
  > *select * from teacher limit 3;*

* #### Change data keys for output  from the table
  > *select id as 'identifier', surname as 'second name' from teacher;*

* #### Sorting data from the table by order
  > *select * from teacher order by surname;*

* #### Sorting data from the table by order DESC
  > *select * from teacher order by id desc;*

* #### Add new key to table
  > *alter table teacher ADD age int;*

* #### Update field in table for all rows
  > *update teacher SET age = 20;*

* #### Update field in table for certain row
  > *update teacher SET age = 20 where id = 1;*

* #### delete certain row in table
  > *delete from teacher where id = 1;*

* #### Get data from the table by substring in the field
  > *select * from teacher where surname LIKE "%ko";*

* #### Get data from the table by condition AND
  > *select * from teacher where id > 2 AND age < 25;*

* #### Get data from the table by condition OR
  > *select * from teacher where id > 5 OR age < 25;*

* #### Get data from the table by inverted value
  > *select * from teacher where NOT id = 2;*

* #### Get data from the table by condition between
  > *select * from teacher where id between 3 and 6;*

* #### Inset array data to the table
  > *insert into lesson (name, teacher_id) values ("Math", 1), ("Inform", 2), ("History", 3), ("Geography", 4), ("Physics", 5), ("Biology", 6), ("Literature", 7);*

* #### Inner join tables
  > *select teacher.surname, lesson.name FROM teacher INNER JOIN lesson ON teacher.id = lesson.teacher_id;*
  > 

* #### Left outer join tables
  > *select teacher.surname, lesson.name FROM teacher LEFT OUTER JOIN lesson ON teacher.id = lesson.teacher_id;*
  > 

* #### Right outer join tables
  > *select teacher.surname, lesson.name FROM teacher RIGHT OUTER JOIN lesson ON teacher.id = lesson.teacher_id;*
  > 

* #### Union join tables (vertical join)
  > *select * from teacher UNION select * from lesson;*
  > 

* #### Function from SQL - get average value
  > *select AVG(age) from teacher;*
  > 

* #### Function from SQL - get min age and max age
  > *select MAX(age), MIN(age) from teacher;*
  > 

* #### Function from SQL - get summary of field from the rows
  > *select SUM(age) from teacher;*
  > 

* #### Function from SQL - get count by field value
  > *select age, COUNT(age) from teacher GROUP by age;*
  > 

  
  
