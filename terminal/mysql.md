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