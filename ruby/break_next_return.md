# Break Next Return

1. Break is to end the loop. In this example it break the each loop:
```ruby
def break_return_next
  a = [1, 2, 3]
  a.each do |n|
    
    unless n != 2
      puts "#{n} is inside unless block"
      break
    end

    puts n
  end
end

break_return_next

# 1
# 2 is inside unless block
# => nil
```

2. Return is to end the process of the break_return_next method.
```ruby
def break_return_next
  a = [1, 2, 3]
  a.each do |n|

    return if n == 1
    
    unless n != 2
      puts "#{n} is inside unless block"
      break
    end

    puts n
  end
end

break_return_next

# => nil
```

3. Next is to end the current iteration and continue with the next each iteration.
```ruby
def break_return_next
  a = [1, 2, 3]
  a.each do |n|
    
    unless n != 2
      puts "#{n} is inside unless block"
      next
    end

    puts n
  end
end

break_return_next

# 1
# 2 is inside unless block
# 3
```

Note: It only puts 2 inside the unless block and not puts at 2 the end.
unless only executed when false
- 1 != 2 => true
- 2 != 2 => false
- 3 != 2 => true