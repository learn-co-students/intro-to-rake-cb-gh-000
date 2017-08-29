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

desc 'loads our environment.rb file'
task  :environment do
  require_relative './config/environment.rb'
end

namespace :db do
  desc 'creates table in db'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds the db with some data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'creates a pry console with access to environment'
task :console => :environment do
  Pry.start
end
