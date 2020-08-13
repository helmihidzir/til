# How to decode url encoded string

eg. `test?value=hello world`. When use `params[:value]`, we will get `hello%20world`.

To solve:
```ruby
require 'uri'

URI.decode(params[:value])
# hello world
```