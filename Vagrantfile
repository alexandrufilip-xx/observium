# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.define :web do |web_config|
    web_config.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "observium"]
    end

    web_config.vm.host_name = "observium"
    web_config.vm.network "private_network", ip: "192.168.100.30"
    # web_config.vm.provision "ansible" do |ansible|
    #     ansible.playbook = "galaxy.yml"
    #     # ansible.verbose = "vvv"
    #   end

   web_config.vm.provision "ansible" do |ansible|
     ansible.playbook = "test.yml"
     ansible.verbose = "vvv"
   end
  end
end
