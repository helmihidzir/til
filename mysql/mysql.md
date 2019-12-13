# MySQL

1. To access mysql shell
```
$ mysql -u root -p
```

2. Grand all privileges to a user account over a specific table from a database
```
mysql> GRANT ALL PRIVILEGES ON database_name.table_name TO 'database_user'@'localhost';
```

3. Revoke privileges
```
mysql> REVOKE ALL PRIVILEGES ON database_name.* TO 'database_user'@'localhost';
```
[Source](https://linuxize.com/post/how-to-create-mysql-user-accounts-and-grant-privileges/)