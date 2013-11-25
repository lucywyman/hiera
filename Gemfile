if gem_source = ENV['GEM_SOURCE']
    source gem_source
else
    source "https://rubygems.org"
end

gem "hiera", :path => File.dirname(__FILE__), :require => false

group :development do
  gem 'watchr'
end

group :development, :test do
  gem 'rake'
  gem 'rspec', "~> 2.11.0", :require => false
  gem 'mocha', "~> 0.10.5", :require => false
  gem 'json', "~> 1.7", :require => false
end

if File.exists? "#{__FILE__}.local"
  eval(File.read("#{__FILE__}.local"), binding)
end

# vim:ft=ruby
