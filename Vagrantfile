# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|

    
    config.vm.box = "geerlingguy/ubuntu2004" # ok
    # config.vm.box = "generic/ubuntu2010"

    # config.vm.box = "ubuntu/focal64"
    # config.vm.box = "ubuntu/bionic64" 
    # config.vm.box = "ubuntu/xenial64"
    # config.vm.box = "ubuntu/trusty64" # ok

    config.vm.box_check_update = false
    config.ssh.insert_key = false
    config.vm.synced_folder ".", "/vagrant", disabled: true 

    # config.vm.hostname = "testing"  
    # config.vm.network :private_network, ip: "192.168.60.4"

    config.vm.provider "virtualbox" do |v|
       v.gui = false
       v.memory = "1024"
       v.linked_clone=true
    end



  # srv server
  config.vm.define "srv-1" do |srv|
    srv.vm.hostname="srv-1.test"
    srv.vm.network :private_network, ip: "192.168.60.3"
  end
  # srv server 2
  config.vm.define "srv-2" do |srv|
    srv.vm.hostname="srv-2.test"
    srv.vm.network :private_network, ip: "192.168.60.4"
  end
  # srv server 3
  config.vm.define "srv-3" do |srv|
    srv.vm.hostname="srv-3.test"
    srv.vm.network :private_network, ip: "192.168.60.5"
  end



  # workstation
  config.vm.define "workstation" do |workstation|
    workstation.vm.hostname="workstation.test"
    workstation.vm.network :private_network, ip: "192.168.60.6"
  end

end