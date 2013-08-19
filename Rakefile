# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = 'wistia-uploader'
  gem.homepage = 'http://github.com/wistia/wistia-uploader'
  gem.license = 'MIT'
  gem.summary = 'A simple CLI uploader for Wistia users.'
  gem.description = 'A simple CLI uploader for Wistia users.'
  gem.email = 'dev@wistia.com'
  gem.authors = ['Robby Grossman', 'Jason Lawrence', 'Brendan Schwartz']
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core/rake_task'
desc 'Run specs'
RSpec::Core::RakeTask.new

task default: :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "wistia-uploader #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
