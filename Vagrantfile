Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "shell",
    :path => "vagrant_specs.sh",
    :upload_path => "/home/vagrant/specs",
    # change <your_role> and <specs_repos> below
    :args => "--install ansible-nginx https://github.com/erasme/erasme-roles-specs"
end
