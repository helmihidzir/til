# object_id

You can call `object_id` method to any variable that you create. `object_id` method will give you value which is a pointer to a location in memory where the actual object data is stored. For example,

```ruby
foo = "bar"
foo.object_id
```