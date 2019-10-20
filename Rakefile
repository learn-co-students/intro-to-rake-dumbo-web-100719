desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end


namespace :db do
  desc 'links our files'
  task :enviroment do
    require_relative './config/environment.rb'
  end

  desc 'migrate changes to your database'
  task :migrate => :enviroment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

  desc 'drop into the Pry console'
  task :console => :enviroment do
    Pry.start
  end
end



# namespace :numbers do
#   def sum(num1, num2)
#     num1+num2
#   end

#   desc 'outputs sum of two numbers'
#   task :sum do
#     puts sum(9, 5)
#   end

#   def squared(num)
#     num**2
#   end

#   desc 'outputs the square of a number'
#   task :squared do
#     puts squared(9)
#   end
# end