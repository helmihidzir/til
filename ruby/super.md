# Super

`super` keyword let you execute the same name method from the parent class of the same method.

```ruby
class Parent
  def say(message)
    p message
  end
end

class Child < Parent
  def say(message)
    super
  end
end

Child.new.say('Hi Rubyist!') # Hi Rubyist!
```

`super()` keyword with parenthesis let you execute parent method without argument. If you use regular `super`, it will give you ArgumentError.

```ruby
class Parent
  def say
    p "I'm the parent"
  end
end

class Child < Parent
  def say(message)
    super()
  end
end

Child.new.say('Hi!') # => "I'm the parent"
```

[source](https://medium.com/rubycademy/the-super-keyword-a75b67f46f05)
