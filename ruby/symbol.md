# Symbol

Symbol is like string but it is not. Symbol is much faster than string.

string = `foo`, symbol = `:foo`

Method can be refer as symbol.

```ruby
class Foo
    def test
        puts "hello"
    end
end

Foo.new.send(:test) # print hello
```

`send` is calling the instance method.
