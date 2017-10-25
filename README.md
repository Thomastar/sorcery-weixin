# Sorcery::Weixin

Sorcery oauth2 provider for https://mp.weixin.qq.com

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'sorcery-weixin'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install sorcery-weixin

## Usage

In your `initializers/sorcery.rb`

``` ruby
require "sorcery/providers/weixin"

# add :weixin provider
config.external_provider = [..., :weixin]

# config weixin
config.weixin.key = "" # appid
config.weixin.secret = "" # appsecret
config.weixin.callback_url = "http://0.0.0.0:3000/oauth/callback?provider=weixin"
config.weixin.user_info_mapping = {nickname: "nickname", gender: "sex", avatar_url: "headimgurl"}
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/xintanghq/sorcery-weixin. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

