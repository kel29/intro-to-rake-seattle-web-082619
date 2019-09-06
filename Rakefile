
namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do

  desc 'migrate changes to your database'
  task :migrate => :environment do
    #the above line creates a task dependency
    #`migrate` depends on the proper environment (below)
    Student.create_table
  end

  task :environment do
    require_relative './config/environment'
  end

  desc 'seed the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

  desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end

  desc 'run console'
  task :console do
    rake console
  end
end
