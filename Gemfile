# frozen_string_literal: true

source 'https://rubygems.org'

eval_gemfile 'Gemfile.devtools'

gemspec

if ENV['USE_SCHEMA_MASTER'].eql?('true')
  gem 'dry-schema', github: 'dry-rb/dry-schema', branch: 'master'
end

if ENV['USE_TYPES_MASTER'].eql?('true')
  gem 'dry-types', github: 'dry-rb/dry-types', branch: 'master'
end

group :test do
  gem 'dry-monads', '~> 1.0'
  gem 'i18n', require: false
end

group :tools do
  gem 'pry', platform: :jruby
  gem 'pry-byebug', platform: :mri
end

group :benchmarks do
  gem 'actionpack'
  gem 'activemodel'
  gem 'activerecord'
  gem 'benchmark-ips'
  gem 'hotch', platform: :mri
  gem 'sqlite3'
  gem 'virtus'
end
