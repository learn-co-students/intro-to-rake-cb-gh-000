namespace :greeting do
  desc "outputs hello to console"
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs hola to console"
  task :hola do
    puts "hola de Rake!"
  end

end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  task :migrate => :environment do
    Student.create_table
  end

  task :seed do
    require_relative './db/seeds.rb'
  end

end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end
