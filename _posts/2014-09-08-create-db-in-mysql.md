---
layout: post
title: Create a Database in mySQL 
tags: sql 
---
I just learnt to create a database in mySQL and I thought of sharing it out here. This post assumes that you have installed mySQL on your computer. 

First you need to connec to mySQL as root. So, in the terminal do the following: 

~~~python

mysql -u root 

~~~

this should start the mySQL program. Now we create a new database: 

~~~python

mysql> create database newbooks;
Query OK, 1 row affected (0.00 sec) 

~~~

This command creates an empty database. The next step is to name the columns of the database: 

~~~python
mysql> create table newbooks (
    -> id INT AUTO_INCREMENT PRIMARY KEY,
    -> Title varchar(20),
    -> Author varchar(20),
    -> CurrentMonthSales int(10));
Query OK, 0 rows affected (0.05 sec)
~~~

To view the description of the table we just created, do the following: 
![My helpful screenshot](/assets/mysql_db_command.jpg)

Now we begin to insert each row. To do this enter each line as a command in mysql: 

~~~python
insert into books values(1,'Pride and Prejudice', 'Austen', 15);
insert into books values(2, 'Animal Farm', 'Orwell', 7);
insert into books values(3, 'Merchant of Venice', 'Shakespeare', 5);
insert into books values(4, 'Romeo and Juliet', 'Shakespeare', 8);
insert into books values(5, 'Oliver Twist', 'Dickens', 3);
insert into books values(6, 'Candide', 'Voltaire', 9);
insert into books values(7, 'The Scarlet Letter', 'Hawthorne', 12);
insert into books values(8, 'Hamlet', 'Shakespeare', 2);
~~~

There we have it, we now have a database table with rows and columns. We can view the table using the basic SQL command: 

~~~python
mysql> select * from newbooks;
+----+---------------------+-------------+-------------------+
| id | Title               | Author      | CurrentMonthSales |
+----+---------------------+-------------+-------------------+
|  1 | Pride and Prejudice | Austen      |                15 |
|  2 | Animal Farm         | Orwell      |                 7 |
|  3 | Merchant of Venice  | Shakespeare |                 5 |
|  4 | Romeo and Juliet    | Shakespeare |                 8 |
|  5 | Oliver Twist        | Dickens     |                 3 |
|  6 | Candide             | Voltaire    |                 9 |
|  7 | The Scarlet Letter  | Hawthorne   |                12 |
|  8 | Hamlet              | Shakespeare |                 2 |
+----+---------------------+-------------+-------------------+
8 rows in set (0.00 sec)
~~~