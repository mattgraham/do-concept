# A sample Guardfile
# More info at https://github.com/guard/guard#readme


guard 'livereload' do
  watch(%r{app/helpers/.+\.rb})
  watch(%r{_site/.+\.(css|js|html)})
  watch(%r{config/locales/.+\.yml})
  # Rails Assets Pipeline
  watch(%r{(_site)(/assets/\w+/(.+\.(css|js|html|png|jpg))).*}) { |m| "/assets/#{m[3]}" }
end
