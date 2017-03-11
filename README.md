# HyperIterator

[Inspired by Ruby Performance Optimization](https://media.pragprog.com/titles/adrpo/iterators.pdf), 
HyperIterator is reimplementation of Ruby iterators in Ruby, designed to address performance 
drawbacks from native implementations, mainly in memory usage.

The main idea is to reduce objects created during iteration, and remove objects from the array while
iterating to speed up garbage collection.

**Caution: this gem monkey patches Ruby's `Array` class.**

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'hyper_iterator'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install hyper_iterator

## Available Methods (adding more)

These methods work just as the non bang version, except that, it **WILL MUTATE** the original array 
by **REMOVING ALL** the elements from it.

- `each_slice!`

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/hyper_iterator. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

