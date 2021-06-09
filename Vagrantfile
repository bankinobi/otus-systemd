# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end
  
  config.vm.define "otus-systemd" do |nfss|
    nfss.vm.network "private_network", ip: "192.168.50.10", virtualbox__intnet: "net1"
    nfss.vm.hostname = "otus-systemd"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
    ansible.become = "true"
  end

end
