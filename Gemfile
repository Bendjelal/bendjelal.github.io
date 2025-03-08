source "https://rubygems.org"

# Jekyll version utilisée par GitHub Pages
gem "jekyll", "~> 3.9"

# Si tu utilises GitHub Pages, active ce gem
gem "github-pages", group: :jekyll_plugins

# Thème du site (supprimer `minima` si tu utilises "so-simple")
gem "jekyll-theme-so-simple"

# Plugins Jekyll
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

# Windows et JRuby
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster pour watching sous Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Correction pour JRuby
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
