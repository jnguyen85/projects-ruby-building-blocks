gem 'rspec', '~>3'
require 'rspec/core/rake_task'

task :default => :spec

desc "Run tests for projects"

desc "run tests for this lab"
RSpec::Core::RakeTask.new do |task|
  lab = Rake.application.original_dir
  task.pattern = "#{lab}/*_spec.rb"
  task.rspec_opts = [ "-I#{lab}", "-I#{lab}/solution", '-f documentation', '-r ./rspec_config']
  task.verbose = false
end
