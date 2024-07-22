source "http://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
# To upgrade, run `bundle update`.

gem "github-pages", group: :jekyll_plugins

gem "webrick", "~> 1.8"
gem "wdm", "~> 0.1.0" if Gem.win_platform?

# If you want to use Jekyll native, uncomment the line below.
gem "jekyll", "~> 3.9.0"

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem 'hawkins'
  gem 'jekyll-gist'
  gem "jekyll-feed"
  gem 'jekyll-sitemap'
  gem 'jekyll-paginate'
  gem 'jekyll-redirect-from'
end

# Time zone correction
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end