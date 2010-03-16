load 'deploy' if respond_to?(:namespace) # cap2 differentiator
Dir['vendor/plugins/*/recipes/*.rb'].each { |plugin| load(plugin) }

load 'config/deploy' # remove this line to skip loading any of the default tasks

set :stages, %w(staging production)
set :default_stage, 'staging'

begin
  require 'capistrano/ext/multistage'
rescue LoadError
  abort "Requires 'capistrano-ext'"
end