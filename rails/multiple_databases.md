# Multiple Databases

1. Database setup in `config/database.yml`

```ruby
development:
  primary:
    database: my_primary_database
    user: root
    adapter: mysql
  secondary:
    database: my_secondary_database
    user: root
    adapter: mysql
    migrations_paths: db/secondary_migrate
```

2. Running specific migration on secondary database

```
 $ rails db:migrate:down:secondary VERSION=20190912104126
```

3. Running migration for secondary database

```
$ rails g migration drop_posts_table --database secondary
```

4. Drop column in the database

```ruby
def change
 drop_table :posts
end
```

5. Migrate on secondary database

```
$ rails db:migrate:secondary
```