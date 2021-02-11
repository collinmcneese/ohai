# frozen_string_literal: true
source "https://rubygems.org"

gemspec

# pull these gems from master of chef/chef so that we're testing against what we will release
gem "chef-config", git: "https://github.com/chef/chef", branch: "master", glob: "chef-config/chef-config.gemspec"
gem "chef-utils", git: "https://github.com/chef/chef", branch: "master", glob: "chef-utils/chef-utils.gemspec"

# yolo master for a bit until they release a ruby-3.0 compatible ffi
gem "ffi", git: "https://github.com/ffi/ffi", branch: "master", submodules: true

# NOTE: do not submit PRs to add pry as a dep, add to your Gemfile.local
group :development do
  gem "chefstyle", git: "https://github.com/chef/chefstyle.git", branch: "master"
  gem "ipaddr_extensions"
  gem "rake", ">= 10.1.0"
  gem "rspec-collection_matchers", "~> 1.0"
  gem "rspec-core", "~> 3.0"
  gem "rspec-expectations", "~> 3.0"
  gem "rspec-mocks", "~> 3.0"
  gem "rubocop-performance", "1.9.0"
  gem "rubocop-rspec"
end

group :debug do
  gem "pry"
  gem "pry-byebug"
  gem "pry-stack_explorer"
  gem "rb-readline"
end
