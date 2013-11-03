# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define :web do |web_config|
      web_config.vm.box = "precise32"
      web_config.vm.network :private_network, ip: "192.168.33.10"

      web_config.vm.provision :ansible do |ansible|
          ansible.playbook = "devops/webserver.yml"
          ansible.inventory_path = "devops/inventory"
      end
  end

  config.vm.define :db do |db_config|
      db_config.vm.box = "precise32"
      db_config.vm.network :private_network, ip: "192.168.33.20"

      db_config.vm.provision :ansible do |ansible|
          ansible.playbook = "devops/dbserver.yml"
          ansible.inventory_path = "devops/inventory"
      end
  end
end
