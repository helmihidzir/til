# Boolean

If the attribute is boolean, Rails will automatically adds question-mark method. For example, `admin` is a boolean data type. In this case Rails add `admin?` method so that we can check the current value of `admin`.

```
>> user = User.first
>> user.admin?
=> false
```