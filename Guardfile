guard :shell do
  watch(/.*\/.*/) do |m|
    system('vagrant ssh -c "specs -p"')
  end
end
