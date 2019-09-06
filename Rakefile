
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
  task :environment do
    require_relative './config/environment'
  end
end

rake db:seed
