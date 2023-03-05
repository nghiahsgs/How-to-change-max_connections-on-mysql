# How-to-change-max_connections-on-mysql
How to change max_connections on mysql

To change the max_connections setting in MySQL, you can follow these steps:

Log in to MySQL as the root user:

```
mysql -u root -p
```
Check the current value of max_connections:

```
SHOW VARIABLES LIKE 'max_connections';
```
To change the value, run the following command:

```
SET GLOBAL max_connections = 1000;
```
Replace 1000 with the maximum number of connections you want to allow.

To make the change permanent, add the following line to the [mysqld] section of your MySQL configuration file (usually located at /etc/mysql/my.cnf):

```
max_connections = 1000
```
Again, replace 1000 with the desired value.

Restart the MySQL service to apply the changes:

```
sudo systemctl restart mysql
```

