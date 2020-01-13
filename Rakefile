# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative 'config/application'

Rails.application.load_tasks

desc 'Update node and yarn version'
task :node_update, [:db_name] do |t|
  system("brew update")
  system("brew upgrade node")
  system("brew link --overwrite node")
  system("brew install yarn")
  system("brew link --overwrite yarn")
end
