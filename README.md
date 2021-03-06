# Ansible Vagrant LAMP

This repository shows how to easily create a Vagrant LAMP server using ansible. It uses Debian 8, Apache 2, PHP7, MySQL 5.6.

# Install

1. Have ansible and vagrant installed.
2. Open shell
3. Execute `vagrant box add debian/jessie64` to download virtual machine
4. Execute `vagrant plugin install vagrant-vbguest` to install VirtualBox guest additions
5. Update `Vagrantfile` if you want to change ip or hostname
6. Add the ip to your hostfile by adding the lines

``` bash
192.168.60.4 dev.site1.com dev.site2.com
```

# Setup

1. Copy `playbook.sample.yml` to `playbook.yml`
2. Make desired changes if you want any to `playbook.yml`
2. Visit project folder in shell
3. Execute `vagrant up --provision` to start and provision machine

# Connect via SSH

1. Visit project folder in shell
2. Execute `vagrant ssh` to enter virtual machine via SSH

# Connect via HTTP

1. Open browser to `http://dev.site1.com` or `http://dev.site2.com`
