# SQLStarter

## Install MySQL locally:

 - SSH to your EC2 Instance

 - install MySQL:

sudo yum install mysql-server

 - start MySQL:

sudo service mysqld start

## Login to MySQL (locally):

mysql -u root -p -h localhost

## Login to MySQL (where the hostname is remote):

mysql -u [db user] -p -h [RDS endpoint hostname]

## Dump the databases:

mysqldump -u root -p [database name] > mysqldump.sql

## Import a database:

mysql -u root -p [database name] -h [RDS endpoint hostname] < mysqldump.sql


# When inside the MySQL terminal:

## Create a database

CREATE DATABASE [databasename];

## Create a table inside a database:

CREATE TABLE [databasename].[tablename] 
(
    id int(10) not null,
    somevarchar varchar(20) not null,
    banana varchar(20)not null
);

## Insert some data

INSERT INTO [databasename].[tablename]() VALUES (1,"Pedro","Banana");

## Show the contents?

SELECT * FROM [databasename].[tablename] where banana="Banana";

## Delete some data?

DELETE FROM [databasename].[tablename]() WHERE banana="Banana";


