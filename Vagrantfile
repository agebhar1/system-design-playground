# -*- mode: ruby -*-
# vi: set ft=ruby :

require 'yaml'

inventory = YAML.load_file('inventory/vagrant.yml')

Vagrant.configure("2") do |config|
  inventory['all']['hosts'].each do |hostname, host_config|
    config.vm.define hostname do |node|

      vm = host_config.dig('vagrant', 'vm')

      node.vm.box = vm['box']
      node.vm.hostname = hostname
      node.vm.network :private_network, ip: host_config['ansible_host']

      config.vm.provider "virtualbox" do |vb|
        vb.gui = vm['gui']
        vb.cpus = vm['cpus']
        vb.memory = vm['memory']
      end

    end
  end
end