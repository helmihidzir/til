# Format in routes (in the `rails routes` command)

For example at `/articles(.:format)`. The `.:format` means what type of format the file being requested.

In controller, if you have 
```ruby
respond_to do |format|
  format.html { ... }
  format.pdf { ... }
  format.json { ... }
end
```
the `.:format` in route will respond respectively to the request being made in the controller.

The parentheses circling the `(.:format)` also means that a given piece of data is optional. If there's a data, it can be called in the controller using `params[:id]`.

[Source](https://stackoverflow.com/questions/20320263/what-does-format-mean-in-rake-routes)