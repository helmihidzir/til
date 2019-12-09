# `routes.rb`

1. If you defined routes do not have `:id`, you can explicitly define it in the routes file. For example,
```ruby
get 'article/:id'
```

2. You can check all the routes in browser by going to `http://localhost:3000/rails/info/routes`

3. Remove unused routes generated from active storage and action mailer when running `rails new` command.
```
rails new blog --skip-active-storage --skip-action-mailer --skip-action-mailbox
```