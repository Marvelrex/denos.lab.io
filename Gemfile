source "https://rubygems.org"

ruby "3.2.3"

gem "jekyll", "~> 4.3"       # was 4.1.1
gem "minima", "~> 2.5"
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"  # bump to a Ruby-3 friendly release
end

platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", platforms: [:mingw, :x64_mingw, :mswin]

gem "webrick", "~> 1.8"      # needed for `jekyll serve` on Ruby 3
