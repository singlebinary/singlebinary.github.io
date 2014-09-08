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