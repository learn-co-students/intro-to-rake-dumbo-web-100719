desc 'grants migrate task access to the environment file'
task :environment do
  require_relative './config/environment'
end
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'drop into the Pry console' #ensures that the Student class and db connection loads first
task :console => :environment do
  Pry.start
end
namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do  #task dependency for Student.create_table
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end


