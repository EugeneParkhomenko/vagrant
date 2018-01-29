# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
   config.vm.box = "bertvv/centos72"
   config.vm.provider "virtualbox" do |vb|
     vb.gui = true
     vb.memory = "512"
   end
   
   config.vm.define "vm1" do |vm1|
	vm1.vm.hostname = "vm1"
	#vm1.vm.network "private_network", ip: "10.0.2.11"
	end
	#config.vm.define "vm2" do |vm2|
	#vm2.vm.hostname = "vm2"
	#vm2.vm.network "private_network", ip: "10.0.2.12"
	#end
   config.vm.provision "shell", 
   inline: <<-SHELL
   yum install mc -y
   yum install git -y
   cd ~vagrant
   mkdir snk
   cd snk
   sudo git clone https://github.com/EugeneParkhomenko/vagrant.git
   cd vagrant
   cat result
      SHELL
   end
   
