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

4. Remove active_storage routes. In `config/application.rb`, replace
```ruby
require 'rails/all'
```
with 
```ruby
require "rails"

# Include each railties manually, excluding `active_storage/engine`
require "active_model/railtie"
require "active_job/railtie"
require "active_record/railtie"
# require "active_storage/engine"
require "action_controller/railtie"
require "action_mailer/railtie"
require "action_view/railtie"
require "action_cable/engine"
require "sprockets/railtie"
require "rails/test_unit/railtie"

```
And then when you try to start the server you will encounter this error.
```
NoMethodError: undefined method `active_storage' for #<Rails::Application::Configuration
```
To fix the error, remove all these line in `config/environments` for each `development.rb`, `production.rb` and `test.rb`.
```
# config.active_storage.service = :local
```