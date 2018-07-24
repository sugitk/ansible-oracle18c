# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "public_network"
  config.vm.hostname = "oracle18c"

  config.vm.provider "virtualbox" do |vbox|
    vbox.name = "oracle18c"
    vbox.cpus = 2
    vbox.memory = "4096"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    # ansible.verbose = "vvv"
  end
end
