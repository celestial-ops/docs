require "bundler/gem_tasks"

namespace :asciidoc do

  desc 'create asciidoc'
  task :create do
    sh 'asciidoctor -a docinfo -a stylesheet! -o dist/latest/index.html docs/main.adoc'
  end

  desc 'publish ascciidoc to gh-pages'
  task :publish => [:create] do
    sh 'ghp-import -m "Generate documentation" -b gh-pages dist/'
    sh 'git push origin gh-pages'
  end

  desc 'clear asciidoc'
  task :clear do
    rm_rf 'dist'
  end
end

