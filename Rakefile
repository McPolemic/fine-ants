require "bundler/gem_tasks"
require "pp"
require "fine_ants"

task :default => :spec

desc 'Download account info for a given adapter'
task :download, [:adapter] do |t, args|
  adapter = args[:adapter]
  raise "Adapter name required!" if adapter.nil?

  pp FineAnts.download(adapter.to_sym, {
    user: ENV.fetch('FINE_ANTS_USERNAME'),
    password: ENV.fetch('FINE_ANTS_PASSWORD')
  })
end
