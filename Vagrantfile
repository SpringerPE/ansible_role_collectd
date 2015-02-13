# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"
  #config.vm.box = "chef/centos-6.5"

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "role.yml"
    ansible.verbose = ""
    ansible.host_key_checking = false
  end
end

