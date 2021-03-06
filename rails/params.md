# Parameters

The `params` method is the object which represents the parameters (or fields) coming in from the form. The `params` method returns an `ActionController::Parameters` object, which allows you to access the keys of the hash using either strings or symbols. [Source](https://guides.rubyonrails.org/getting_started.html#creating-articles)

To see the what the parameters looks like you can run
```ruby
def create
  render plain: params[:article].inspect
end
```

and it will return
```
<ActionController::Parameters {"title"=>"First Article!", "text"=>"This is my first article."} permitted: false>
```

---

The way to set a query parameter in Rails is to include a hash in the named route, in this example email hash is included:

`edit_account_activation_url(@user.activation_token, email: @user.email)`

This also will give `params[:email]` in the controller to be access.