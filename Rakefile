
task :environment do
  require_relative './config/environment'
end

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'creates students table'
  task :migrate  => :environment do
    Student.create_table
  end

  desc 'populates db with dummy data from a file'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
