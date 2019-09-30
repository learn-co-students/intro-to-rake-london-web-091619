namespace :greeting do
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

task :hola do
  puts "hola de Rake!"
end
end

desc 'drop into the pry console'
task :console => :environment do
  pry.start
end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
end

namespace :db do
  desc 'puts seed data into table'
  task :seed do
    require_relative './db/seeds.rb'
  end
end