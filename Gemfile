source 'https://rubygems.org'

gem 'jekyll'

group :jekyll_plugins do
  gem 'jekyll-gist'
  gem 'jekyll-paginate'
  gem "jekyll-asciidoc"
  gem "font_awesome"
end

gem 'asciidoctor', '~> 1.5.4'
gem 'coderay', '1.1.1'

require 'rbconfig'
if RbConfig::CONFIG['target_os'] =~ /darwin(1[0-3])/i
   gem 'rb-fsevent', '<= 0.9.4'
end
