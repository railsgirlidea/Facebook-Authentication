Facebook Connect Integration Using Devise and OmniAuth In Rails App.

For this I included gem
  gem ‘devise’
  gem 'omniauth'
  gem 'omniauth-facebook' 

First of all you need to create an app in facebook to get “App-ID” and “App Secret”
  https://developers.facebook.com/

Now you need to declare the provider name and app id and key.Go to the file config/initializers/devise.rb and the following line

require "omniauth-facebook"
config.omniauth :facebook, "APP_ID", "APP_SECRET"

And then You create a link in Your layout/application.html.erb
  <%= link_to "Sign in with Facebook", user_omniauth_authorize_path(:facebook) %>