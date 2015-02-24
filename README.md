# Viral

Viral is a simple game designed for you to have fun making computer viruses without all of the drama. In the real world, hacking leads to tedious social engineering, incarceration, and existential crises. With Viral, you don't have to worry about any of that: just write the code, infect, and see how fast your friends can erradicate your virus. 

## Installation

First, install VirtualBox and Vagrant.

Then, add this line to your application's Gemfile:

```ruby
gem 'viral'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install viral

## Usage

Viral is primarily intended for command line usage, but if you want to develop programs that use Viral, a Ruby interface is available. Viruses are written in Ruby, and network definitions are written in YAML. 

Here is a basic virus:

```ruby
Virus.new do
  puts 'Hello, world!'
end
```

Here is a simple network definition.

```yaml
nodes:
  - hostname: ubuntubox 
    os: Ubuntu
    connections: [debianbox]
  - hostname: debianbox
    os: Debian 
    connections: [ubuntubox]
```

To run this virus in the given network, use `viral virus.rb network.yaml`.

More information on viruses and network definitions is available in the documentation and in the wiki.

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release` to create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

1. Fork it ( https://github.com/[my-github-username]/viral/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
