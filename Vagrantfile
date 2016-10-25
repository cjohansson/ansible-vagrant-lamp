# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  # General Vagrant VM configuration
  config.vbguest.auto_update = true
  config.vm.box = 'debian/jessie64'
  config.ssh.insert_key = false
  config.vm.synced_folder '../.', '/var/www', owner: 'www-data', group: 'www-data'
  config.vm.provider :virtualbox do |v|
    v.memory = 256
    v.linked_clone = true
  end

  # Web server 1.
  config.vm.define 'web1' do |app|
    app.vm.hostname = 'cvj-web1.dev'
    app.vm.network :private_network, ip: '192.168.60.4'
  end

  # Ansible
  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'playbook.yml'
  end
end
