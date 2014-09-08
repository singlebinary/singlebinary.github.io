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
create table books (
id INT AUTO_INCREMENT PRIMARY KEY,
Title varchar(20), 
Author varchar(20),
CurrentMonthSales int(10));
~~~

To view the description of the table we just created, do the following: 

~~~python 
mysql> desc newbooks;
+-------------------+-------------+------+-----+---------+----------------+
| Field             | Type        | Null | Key | Default | Extra          |
+-------------------+-------------+------+-----+---------+----------------+
| id                | int(11)     | NO   | PRI | NULL    | auto_increment |
| Title             | varchar(20) | YES  |     | NULL    |                |
| Author            | varchar(20) | YES  |     | NULL    |                |
| CurrentMonthSales | int(10)     | YES  |     | NULL    |                |
+-------------------+-------------+------+-----+---------+----------------+
4 rows in set (0.00 sec)
~~~