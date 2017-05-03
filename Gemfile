source "https://rubygems.org"

ruby "2.3.1"

gem "autoprefixer-rails"
# gem "delayed_job_active_record"
gem "flutie"
gem "jquery-rails"
gem "pg"
gem "puma"
gem "rack-canonical-host"
gem "rails", "~> 5.0.2"
gem "recipient_interceptor"
gem "sass-rails", "~> 5.0"
gem "sprockets", ">= 3.0.0"
gem "uglifier"
gem "turbolinks"

gem "aws-sdk"

gem "solidus", "~> 2.2.0.rc1"
gem "solidus_auth_devise"
gem "solidus_i18n", github: "solidusio-contrib/solidus_i18n", branch: "master"
gem 'globalize', github: 'globalize/globalize'
gem 'solidus_globalize', github: 'AndreiMotinga/solidus_globalize', branch: "fixes"

group :development do
  gem "spring"
  gem "spring-commands-rspec"
  gem "web-console"
end

group :development, :test do
  gem "awesome_print"
  gem "bullet"
  gem "bundler-audit", ">= 0.5.0", require: false
  gem "dotenv-rails"
  gem "factory_girl_rails"
  gem "pry-byebug"
  gem "pry-rails"
  gem "rspec-rails", "~> 3.5.0.beta4"
end

group :development, :staging do
  gem "rack-mini-profiler", require: false
end

group :test do
  gem "capybara-webkit"
  gem "database_cleaner"
  gem "formulaic"
  gem "launchy"
  gem "shoulda-matchers"
  gem "simplecov", require: false
  gem "timecop"
  gem "webmock"
end

group :staging, :production do
  gem "rack-timeout"
  gem "rails_stdout_logging"
end
