# MySQL

1. Enter into MySQL cli
```bash
mysql -u root -p
```

`-u` - for user
`-p` - if your mysql have password

2. Start MySQL server (if installed using Homebrew)
```bash
brew services start mysql
```

3. Stop MySQL server (if installed using Homebrew)
```bash
brew services stop mysql
```

4. Grand all privileges to a user account over a specific table from a database
```
mysql> GRANT ALL PRIVILEGES ON database_name.table_name TO 'database_user'@'localhost';
```

5. Revoke privileges
```
mysql> REVOKE ALL PRIVILEGES ON database_name.* TO 'database_user'@'localhost';
```
[Source](https://linuxize.com/post/how-to-create-mysql-user-accounts-and-grant-privileges/)

6. Error mysql
```
ERROR 1698 (28000): Access denied for user 'root'@'localhost'
```

Solution:
Error occured because root is authenticate via auth_socket
```
sudo mysql
mysql> SELECT user,authentication_string,plugin,host FROM mysql.user;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
```
[Source](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-18-04)