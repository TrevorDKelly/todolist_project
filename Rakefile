require 'rake/testtask'
require 'find'
require 'bundler/gemtasks'

desc 'Run tests'
task :default => [:test]

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task"
end

Rake::TestTask.new(:test) do |t|
  t.libs << 'test'
  t.libs << 'lib'
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'Show non-hidden files'
task :files do
  Find.find('./') do |path|
    next if path.include?('/.')
    puts path if File.file?(path)
  end
end
