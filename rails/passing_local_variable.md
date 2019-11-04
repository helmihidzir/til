# Passing local variable

Passing instance variable to another partial or view.

```ruby
render '<controller>/<method>', locals: { error: @<instance variable name> }
```

For example, you have `post` controller. Inside the controller you have `create` method but then when the `create` method fails to create new post, you want to completely render new and different page which is in this case `fail.html.erb` views.

```ruby
def create
    @post = current_user.posts.build(post_params)
    if @post.save
      redirect_to root_path, notice: "Successfully created a new Post!"
    else
      render 'posts/fail', locals: { error: @post.errors.full_messages }
    end
end
```

In `fail.html.erb` you can call the variable `error`.
```
<%= error %>
```