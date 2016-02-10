source 'https://rubygems.org'

gemspec

platforms :ruby, :mswin, :mingw do
  case ENV['DB']
  when 'postgresql'
    gem 'pg'
  when 'mysql'
    gem 'mysql2'
  when 'sqlite'
    gem 'sqlite3'
  else
    gem 'sqlite3'
  end
end

platforms :jruby do
  gem 'activerecord-jdbcmysql-adapter', '>= 1.2'
  gem 'jdbc-mysql', '>= 5.1'
  gem 'activerecord-jdbcpostgresql-adapter', '>= 1.2'
  gem 'jdbc-postgres', '>= 9.2'
  gem 'activerecord-jdbcsqlite3-adapter', '>= 1.3.0.beta1'
  gem 'jdbc-sqlite3', '>= 3.7'
end

group :test do
  gem 'database_cleaner', ['>= 1.2', '!= 1.4.0', '!= 1.5.0']
  gem 'factory_girl', '>= 4.2'
  gem 'rspec-rails', '>= 2.14'
  gem 'rubocop', '~> 0.31.0'
  gem 'codeclimate-test-reporter', require: nil
end
