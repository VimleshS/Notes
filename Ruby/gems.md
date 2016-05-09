# Gems

```
// How many gems do you have
▶ grep -c '^\s*gem' Gemfile
▶ bundle list | grep -c '\*'
```

* [Exploring the Structure of Ruby Gems](https://blog.codeship.com/exploring-structure-ruby-gems/)
* [pHash - Perceptual hash library for detecting duplicate multimedia files](https://github.com/westonplatter/phashion)
* [Feature switch](https://github.com/pda/flip)
* [SimpleCalendar](https://gorails.com/blog/simplecalendar-1-1-released)
* [Marketing email](https://www.mailerlite.com)
* [Pundit - Minimal authorization through OO design](https://github.com/elabs/pundit)
* [prawn-svg](https://github.com/mogest/prawn-svg)
* [Reform - Form Object](https://github.com/apotonick/reform)
* [money from Shopify](https://github.com/Shopify/money) - See all Shopify's open source projects at [here](http://shopify.github.io/)
* [Money](http://rubymoney.github.io/money/)
* [Simple immutable Value Objects for Ruby](https://github.com/tcrayford/values)
* [rails_12factor](https://github.com/heroku/rails_12factor)
* [keyset pagination](https://github.com/glebm/order_query)
* [hiredis - for better redis performance](https://github.com/redis/hiredis-rb)
* [IP geolocation - Go language actually](https://github.com/fiorix/freegeoip)
* [ransack - Object-based searching (rewrite of MetaSearch)](https://github.com/activerecord-hackery/ransack)
* [accepts_nested_ids](https://github.com/uberllama/accepts_nested_ids)
* [**Queue using NSQ**](https://github.com/wistia/nsq-ruby)
* [Facets](https://github.com/rubyworks/facets)
* [simple_command](https://github.com/nebulab/simple_command)

## Required Gems in new project

```ruby
group :development do
  gem 'puma'

  gem 'quiet_assets'
  gem 'awesome_print'

  gem 'better_errors'
  gem 'binding_of_caller'
  
  gem 'money'

  gem 'pry-rails'

  gem 'rails_best_practices'
  gem 'brakeman', require: false
  gem 'rubocop'
  gem 'sandi_meter'
  gem 'rubycritic', require: false

  gem 'bullet'
  
  gem 'rack-mini-profiler', require: false
end
```

## Performance gems

Always profile in production mode as development will produce all kinds of garbage in order to support hot reloading.

* [memory_profiler](https://github.com/SamSaffron/memory_profiler)
* [allocation_tracer](https://github.com/ko1/allocation_tracer)

## Bundler

* Constraint satisfaction
* Depth-first search and Backtracking

```
▶ bundle binstubs spec-core
▶ bin/rspec

// Repeat as needed for other gems
```

* [How does Bundler work, anyway?](https://www.youtube.com/watch?v=GvFfd_MCJq0)
* [Bundler: The easy, the hard, and the NP-complete](https://www.youtube.com/watch?v=3soqhbnh0jY)

```ruby
require 'ruby gems'
require 'bundler'
Bundler.setup
Bundler.require
```

## Authentication and Authorization gems

* [access-granted](https://github.com/chaps-io/access-granted)
* [proof](https://github.com/undercase/proof)

## Validation gems

* [strip_attributes](https://github.com/rmm5t/strip_attributes)
* [auto_strip_attributes](https://github.com/holli/auto_strip_attributes)
* [Cleaner validations using the Either monad](https://blog.abevoelker.com/you-got-haskell-in-my-ruby-cleaner-ruby-validations-using-either-monad-kleisli-gem/)

## Date gems

* [stamp](https://github.com/jeremyw/stamp)
* [business_time](https://github.com/bokmann/business_time)
* [Holidays - Using YAML file](https://github.com/alexdunae/holidays)
* [working_hours](https://github.com/Intrepidd/working_hours)
* [workpattern](https://github.com/callenb/workpattern)

## API wrapper gems

* [How to create a wrapper gem for service APIs](https://gregmoreno.wordpress.com/2012/06/07/how-to-create-a-wrapper-gem-for-service-apis-part-1/)
* [Wrapping your API in a custom Ruby gem](https://blog.engineyard.com/2014/wrapping-your-api-in-a-ruby-gem)
* [Writing an API wrapper in Ruby with TDD](http://code.tutsplus.com/articles/writing-an-api-wrapper-in-ruby-with-tdd--net-23875)
* [Ruby API wrapper using Virtus and Typhoeus](http://www.nickdesteffen.com/blog/ruby-api-wrapper-using-virtus-and-typhoeus)
* [Pact: TDD for API](https://github.com/realestate-com-au/pact)

## API wrapper examples

* [Reddit](https://github.com/samsymons/RedditKit.rb)