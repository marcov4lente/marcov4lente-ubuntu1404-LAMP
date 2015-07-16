Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "4096"]
  end

  config.vm.network "private_network", ip: "192.90.90.90"

  config.vm.synced_folder "/Users/marco/Projects", "/var/www" , :mount_options["dmode=777,fmode=777"]
  config.vm.provision :shell, path: "bootstrap.sh"
end
