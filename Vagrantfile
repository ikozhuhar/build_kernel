# -*- mode: ruby -*-
# vi: set ft=ruby :

$mach_quant = 10

ENV['VAGRANT_SERVER_URL'] = 'https://vagrant.elab.pro'

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1
  end

  (1..$mach_quant).each do |i|
      config.vm.define "node#{i}" do |node|
          node.vm.network "public_network", ip: "192.168.1.#{24+i}"
          node.vm.hostname = "node#{i}"
      end
  end

end
