# -*- mode: ruby -*-
# vi: set ft=ruby

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
#  config.vm.box = "centos/7"  
  config.vm.network :private_network, ip: "192.168.33.10"
#  config.vm.network :forwarded_port, guest: 80, host: 8080 
  config.vm.provision "ansible" do |ansible|
    ansible.limit = "all"
    ansible.verbose = "v"
    ansible.playbook = "site.yml"
    ansible.inventory_path = "hosts"
  end
end
