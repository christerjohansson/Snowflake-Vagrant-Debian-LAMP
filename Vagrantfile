# -*- mode: ruby -*-
# vi: set ft=ruby :

# Basic configuration of the machine
Vagrant.configure("2") do |config|
  config.vm.box = "rockschtar/box"
  config.vm.box_version = "1.0"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.hostname = "snowflake.dev"
  config.vm.network "forwarded_port", guest: 22, host: 2200, host_ip: "127.0.0.1", id: "ssh"
  config.vm.synced_folder "./public", "/var/www/html", :nfs => { :mount_options => ["dmode=777","fmode=666"] }
 
# Custom configuration for the VirtualBox. Change if you need to.
  config.vm.provider "virtualbox" do |v|
  v.memory = 2048
  v.customize ["modifyvm", :id, "--cableconnected1", "on"]
  v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  v.customize ["modifyvm", :id, "--nictype1", "Am79C973"]
end
end
