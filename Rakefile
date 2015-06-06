
require 'csv'
# require 'nokogiri'
# require 'open-uri'
require 'yaml'


desc "Convert waste streams CSV into YAML"
task :streams do
  lines = CSV.read('_data/wrap_material_streams.csv')
  streams_def = {}
  lines.shift
  lines.each do |line|
    streams_def[line[0]] = { 'parent' => line[1], 'color' => line[2] }
    # puts streams_def.to_yaml
    File.open("_data/material_streams.yml", "w") { |file| file.write(streams_def.to_yaml) }
  end
end
