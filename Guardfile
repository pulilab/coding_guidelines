notification :off

guard 'livereload' do
  watch(%r{^build/html/.+\.(html)$})
  watch(%r{^build/html/_static/.*$})
end


# Add files and commands to this file, like the example:
#   watch(%r{file/path}) { `command(s)` }
#
guard 'shell' do
  watch(%r{(.*)\.rst}) do |m|
    system("make html")
  end
end
