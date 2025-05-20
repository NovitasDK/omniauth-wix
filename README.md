This fork was created to change the way the original gem generates the callback_path.

The reason for this is because we're using omniauth-google-oauth2 to sign in with Google, and when this is registered into the devise routes, it hijacks all requests beginning with "auth" and prepends "users". This broke the original, unforked version.

---

# Omniauth::Wix

Wix Strategy for OmniAuth 2.0

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'omniauth-wix'
```

And then execute:

    $ bundle install

Or install it yourself as:

    $ gem install omniauth-wix

## Usage

Depends on https://github.com/omniauth/omniauth

Setup OAuth credentials at https://dev.wix.com/

Here's a quick example, adding the middleware to a Rails app in config/initializers/omniauth.rb:

Rails.application.config.middleware.use OmniAuth::Builder do
  provider :wix, ENV['WIX_APP_ID'], ENV['WIX_APP_SECRET']
end

Authenticate the user by having them visit /auth/wix

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/pixetree/omniauth-wix.

