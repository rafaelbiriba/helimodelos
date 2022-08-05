task :server do
  sh "open 'http://127.0.0.1:4000/blog/' && bundle exec jekyll serve --host 0.0.0.0 -c config/jekyll_config.yml --livereload --watch --drafts --unpublished"
end

task :publish do
  ARGV.shift

  sh "bundle exec jekyll build --config config/jekyll_config.yml,config/jekyll_config_production.yml #{ARGV.first}"
end

task :post do
  ARGV.shift

  sh "JEKYLL_EDITOR=code bundle exec jekyll compose --config config/jekyll_config.yml post #{ARGV.first}"
end