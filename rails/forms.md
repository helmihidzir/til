# Forms

How does Rails know to use a `POST` request for new users and a `PATCH` for editing users?

By using Active Record's `new_record?` boolean method. If `new_record?` return true, Rails uses `POST`, if it returns false, Rails use `PATCH`.

[Code](https://github.com/rails/rails/blob/b081f6b59fb3f15d12043072ad9b331ffd2bc56e/activerecord/lib/active_record/persistence.rb#L64)

[Rails tutorial explanation](https://www.learnenough.com/ruby-on-rails-4th-edition-tutorial/updating_and_deleting_users#sec-updating_users)(Scrol down a bit in updating users section)