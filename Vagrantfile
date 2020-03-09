# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.define "controller" do |node|
          node.vm.box = "bento/amazonlinux-2"
          node.vm.hostname = "controller"
          node.vm.network :private_network, ip: "192.168.101.10"
          node.vm.network :forwarded_port, id: "ssh", guest: 22, host: 2210
    end
    config.vm.define "target" do |node|
          node.vm.box = "bento/amazonlinux-2"
          node.vm.hostname = "target"
          node.vm.network :private_network, ip: "192.168.101.20"
          node.vm.network :forwarded_port, id: "ssh", guest: 22, host: 2220
          # For Ruby on Rails App
          node.vm.network :forwarded_port, guest: 3000, host: 3030

    end
  end
