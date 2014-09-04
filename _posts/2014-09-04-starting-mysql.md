---
layout: post
title: Starting mySQL on Mac 
tags: sql 
---
This is something that happens to new SQL users. "I installed mySQL with Homebrew. Now: 

1.  How do I start mysql session? 
    It is as easy as typing 'mysql'
2.  When I reboot my computer and type 'mysql' I get the following message "ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/tmp/mysql.sock". Why is this? 
The answer to question is very simple: start the sql server in the following way: mysql.server start. Once you have it, type mysql and violà, we have the mysql server running. 

I hope this helps people who are trying to find the answer to their problems. 