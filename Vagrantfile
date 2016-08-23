# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 8000, host:8000

  config.vm.provision "ansible" do |ansible|
    ansible.playbook="provision/provisioner.yml"
  end
  
  config.vm.synced_folder "./project", "/home/django/project", mount:false

end
