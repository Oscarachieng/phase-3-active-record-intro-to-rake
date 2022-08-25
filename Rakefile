
namespace :greeting do 
desc 'printing hola from the terminal'
task :hola do
  puts 'hola de Rake!'
end

desc 'outputing hello from the terminal'
task :hello do
  puts "hello from Rake!"
end
end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  task migrate: :environment do
    Student.create_table
  end
   desc "Seeding our database"
  task seed: :environment do
    require_relative './db/seeds'
  end
end

desc "getting into the pry console"
task console: :environment do 
  pry.start
end
