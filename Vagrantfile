Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.define "nginx" do |nginx|
  end
  config.vm.provision "shell",
    :path => "vagrant_specs.sh",
    :upload_path => "/home/vagrant/specs",
    # change role name below
    :args => "--install ansible-nginx"
end
