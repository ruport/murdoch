require "rake/rdoctask"
require "rake/testtask"
require "rake/gempackagetask"

begin
  require "rubygems"
rescue LoadError
  nil
end

spec = Gem::Specification.new do |spec|
  spec.name = "murdoch"
  spec.version = "1.0.1"
  spec.platform = Gem::Platform::RUBY
  spec.summary = "A generalized Ruby report generation and templating engine."
  spec.files =  Dir.glob("lib/**/**/*")+["Rakefile"]
  spec.require_path = "lib"
  
  spec.test_files = Dir[ "test/*_test.rb" ]
  spec.has_rdoc = true
  spec.add_dependency('activerecord')
  spec.add_dependency('ruport', '= 1.6.1')
  spec.add_dependency('ruport-util','= 0.14.0')
  spec.add_dependency('acts_as_reportable', '= 1.1.1')
  spec.author = "Gregory Brown"
  spec.email = "gregory.t.brown@gmail.com"
  spec.rubyforge_project = "ruport"
  spec.homepage = "http://rubyreports.org"
  spec.description = <<END_DESC
  Ruby Reports is a software library that aims to make the task of reporting
  less tedious and painful. It provides tools for data acquisition,
  database interaction, formatting, and parsing/munging.
END_DESC
end

Rake::GemPackageTask.new(spec) do |pkg|
  pkg.need_zip = true
  pkg.need_tar = true
end

