# middleman-remove-indent

[![Gem Version](https://badge.fury.io/rb/middleman-remove-indent.svg)](http://badge.fury.io/rb/middleman-remove-indent)
[![Build Status](https://travis-ci.org/yterajima/middleman-remove-indent.svg?branch=master)](https://travis-ci.org/yterajima/middleman-remove-indent)

`middleman-remove-indent` is an extension of [Middleman](http://middlemanapp.com/).  
This extension remove indent from build files (ex: .html, .css).

## Installation

Add this line to your application's Gemfile:

    gem 'middleman-remove-indent'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install middleman-remove-indent

## Usage

In `config.rb`:

```ruby
configure :build do
  activate :remove_indent
end
```

Then `middleman-remove-indent` remove indent from `build/\*.html`, `build/\*.css`.  
if you want to remove indent only `.html`, you could change `:exts` option:

```ruby
configure :build do
  activate :remove_indent, :exts => %w(.html) # default:  %w(.html .css)
end
```

if you want to remove BLANK LINE too, you could do with `:remove_blank_line' option:

```ruby
configure :build do
  activate :remove_indent, :remove_blank_line => true # default: false
end
```

## Contributing

1. Fork it ( http://github.com/yterajima/middleman-remove-indent/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

