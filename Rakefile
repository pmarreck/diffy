require 'spec/rake/spectask'
require 'rake/rdoctask'
require 'rake/gempackagetask'

task :default => :spec

desc "Run all specs in spec directory"
Spec::Rake::SpecTask.new(:spec) do |t|
  t.spec_files = FileList['spec/**/*_spec.rb']
end

Rake::RDocTask.new do |rd|
  rd.main = "README"
  rd.rdoc_dir = 'doc'
  rd.rdoc_files.include("README", "**/*.rb")
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |s|
    s.name = %q{dirb}
    s.version = "0.1.0"

    s.required_rubygems_version = Gem::Requirement.new(">= 0") if s.respond_to? :required_rubygems_version=
    s.authors = ["Sam Goldstein"]
    s.date = %q{2010-06-28}
    s.description = %q{Convenient diffing in ruby}
    s.email = %q{sgrock@gmail.com}
    s.has_rdoc = true
    s.homepage = "http://github.com/samg/dirb/tree/master"
    s.rdoc_options = ["--inline-source", "--charset=UTF-8"]
    s.require_paths = ["lib"]
    s.summary = %q{A convenient way to diff string in ruby}

    if s.respond_to? :specification_version then
      current_version = Gem::Specification::CURRENT_SPECIFICATION_VERSION
      s.specification_version = 2

      if Gem::Version.new(Gem::RubyGemsVersion) >= Gem::Version.new('1.2.0') then
        s.add_runtime_dependency(%q<mime-types>, [">= 1.16"])
        s.add_runtime_dependency(%q<diff-lcs>, [">= 1.1.2"])
      else
        s.add_dependency(%q<mime-types>, [">= 1.16"])
        s.add_dependency(%q<diff-lcs>, [">= 1.1.2"])
      end
    else
      s.add_dependency(%q<mime-types>, [">= 1.16"])
      s.add_dependency(%q<diff-lcs>, [">= 1.1.2"])
    end
  end
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install technicalpickles-jeweler -s http://gems.github.com"
end

