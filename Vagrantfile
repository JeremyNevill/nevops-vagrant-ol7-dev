# -*- mode: ruby -*-
# vi: set ft=ruby :

# See https://yum.oracle.com/boxes/ for Oracle Vagrant Boxes
NAME = "nevops-vagrant-ol7-dev"
VBOX_URL = "https://oracle.github.io/vagrant-projects/boxes"
VBOX_NAME = "oraclelinux/7"

Vagrant.configure("2") do |config|

    # Vagrant Box (Oracle Linux 7) with Minimal Dev Tools 
    # ===================================================
    config.vm.box = VBOX_NAME
    config.vm.box_url = "#{VBOX_URL}/#{VBOX_NAME}.json"
    config.vm.network "forwarded_port", guest: 8081, host: 8081
  
    config.vm.provider "virtualbox" do |vb|
       # vb.gui = true
       vb.memory = 2048
       vb.name = NAME
    end
  
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "ol7-dev.yml"
    end
  
  end