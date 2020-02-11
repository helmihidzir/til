# Arguments

What is arguments?

1. Arguments is when you call method and give it parameter. Example:

   ```
   def foo(bar) # bar is call parameter here, because this is method definition.
       puts bar
   end

   foo(bar) # print bar
   # foo is the method and bar is call argument here, because this is method call.
   ```

2. There are few types of arguments. Example:

   ```
   def foo(a, b, bar: "default", bell: "default")
       puts "#{a} #{b} #{bar} #{bell}"
   end

   foo("I", "love", bell: "helmi", bar: "you") # print I love you helmi
   foo("love", "I", bell: "helmi", bar: "you") # print love I you helmi
   ```

   a and b is positional argument while bar and bell is keyword argument. Positional argument means that the value will affected by the position of argument while keyword argument do not affected about the position.
