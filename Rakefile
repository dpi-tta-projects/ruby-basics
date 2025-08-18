#!/usr/bin/env ruby

require 'bundler/setup'
require 'rake'
require 'grade_runner'

dir = Gem::Specification.find_by_name('grade_runner').gem_dir
load "#{dir}/lib/tasks/grade.rake"

GradeRunner.config do |config|
  config.override_local_specs = false

  # TODO: update submission url to production grades.dpi.dev
  config.submission_url = "https://3dbe9c3c0f53.ngrok-free.app"
end

Rake::Task[ARGV[0]].invoke
