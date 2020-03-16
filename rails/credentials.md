# Credentials

Rails credentials can be seen by running this command
```bash
EDITOR="nano" rails credentials:edit
```

Then, it will open `config/credentials.yml.enc`
```
# for example
username: helmi

development:
    postgres_username: your_name
    postgres_password: your_pasword
```

To use the save credentials in ruby, call it like this
```ruby
Rails.application.credentials.username # helmi
Rails.application.credentials.dig(:development, :postgres_username) # your_name
```

but if you want to call it in yaml file use it like this
```
<%= Rails.application.credentials.dig(:development, :postgres_username) %>
```