# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

vmname="nodejs"
ipaddr="192.168.33.23"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos65"
  config.vm.box_url = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"
  config.vm.hostname = vmname
  config.vm.network :private_network, ip: ipaddr
  config.vm.boot_timeout = 300
  config.vm.provider :virtualbox do |vb|
    vb.name = vmname
    # vb.gui = true
    vb.customize ["modifyvm", :id, "--cpus", 2]
    vb.customize ["modifyvm", :id, "--memory", 1024]
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "off"]
  end
end
