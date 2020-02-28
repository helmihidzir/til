# Tips and tricks for new developer 
[source](https://www.youtube.com/watch?v=BZbW8FAvf00&t=344s)

1. Copy all configuration, secrets or database
   ```
   $ cp config/database.yml config/database.sample.yml
   $ echo "config/database.yml" >> .gitignore
   
   $ cp config/secrets.yml config/secrets.sample.yml
   $ echo "config/secrets.yml" >> .gitignore
   ```
   
2. We can have as many as we want for configuration file. For example,
   `config/payments.yml`
   ```
   development:
        stripe_key: 123456
   
   test: 
        stripe_key: 123456
   
   production: 
        stripe_key: <%= ENV['STRIPE_KEY']
   ```
   Then we can call it in the application with `Rails.application.config_for(:payments)['stripe_key']`
   
3. Use constant when have fixed string or integer or move to configuration file if it is change consistently.
    ```
    REGISTRATION_LIMIT = 30
   
   if registered_at < REGISTRATION_LIMIT.minutes.ago
        #...
   end
    ```

4. Do not ignore `db/schema.rb` or problem occured. Use `$ rails db:setup` or `$ rails db:reset`

5. Be careful when change data in migration file.

6. Prefer SQL over ruby in some cases.

7. Do not pass object to background jobs. Because object is large. Better to pass only id for reference to object.
   ```
   class BigBadJob
        def perform(order_id, user_id)
            order = Order.find(order_id)
            user = User.find(user_id)
        end   
   end
   ```

8. Deliver your email later.

9. Be RESTful all the time. `index show new create edit update delete`. From `deactivate` method in `ProductsController` 
to `update` method in `ProductStatesController`.Another example, from `apply_coupon` method in `CartsController` 
to `create` method in `DiscountsController`.

10. Recommended ruby gems.

    - rubocop (for styling)
    - annotate (for reference of data types and column of model)
    - bullet (telling what's weird in your code)
    - oink (detect memory leak)