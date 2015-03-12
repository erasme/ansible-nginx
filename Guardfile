# -- -*- mode: ruby; -*-

guard :shell do
  watch(%r{^*/.*\.yml$}) do |m|
    system('vagrant ssh -c "specs -p"')
  end
end
