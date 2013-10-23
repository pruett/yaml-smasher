module Yaml
  require 'yaml'
  class Smash < Thor
    include Thor::Actions

    desc "file /path/to/file.yml", "Smash up a .yml file into individual folders"
    method_options force: :boolean, desc: "Forcefully overwrite homie"
    def file(file)
      create_folders_from(YAML.load_file(file), options.force?)
    end

    no_commands do
      def create_folders_from(yaml_arr, force)
        yaml_arr.each_with_index do |obj, i|
          folder = obj["folder"] || "folder#{i}"
          filename = obj["filename"] || "filename#{i}"

          content = "-\n"
          obj.each do |key, value|
            unless key == "product" || key == "filename"
              content += "\t#{key}: #{value}\n"
            end
          end
          create_file "#{folder}/#{filename}.yml" do
            content
          end
        end
      end
    end

  end
end