# Form with helper

```ruby
<%= form_with(url: "/search", method: "get") do %>
  <%= label_tag(:q, "Search for:") %>
  <%= text_field_tag(:q) %>
  <%= submit_tag("Search") %>
<% end %>
```

`form_with` is a actually a ruby method.

`form_with (url: "/search", method: "get")`. All of these is a method and inside the parentheses`()` is hash parameters. `url:` and `method:` are hash parameters aka keys. `/search` and `"get"` are their values respectively. The `do` until the `end` is a block. I just learned that methods can have a block.

---

Parameters aka arguments also?

it is a matters of perspective. Parameters is when method definitions while arguments is when method call. [source](https://rorguide.blogspot.com/2011/06/difference-between-argument-and.html)
