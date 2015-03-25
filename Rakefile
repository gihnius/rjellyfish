require "bundler/gem_tasks"
require 'rake/extensiontask'
require 'rake/testtask'

GEMSPEC = Gem::Specification.load(File.expand_path("../jellyfish.gemspec", __FILE__))

Rake::ExtensionTask.new('cjellyfish', GEMSPEC) do |ext|
  ext.name    = 'jellyfish'
  ext.lib_dir = 'lib/jellyfish'
end

Rake::TestTask.new do |t|
  t.libs << 'test'
end

desc "Run tests"
task :default => :test
