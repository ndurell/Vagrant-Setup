# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "jdrydn/trusty"
  config.vm.network :forwarded_port, host: 8080, guest: 8080
  config.vm.synced_folder "/Users/ndurell/work/shoobx", "/home/vagrant/shoobx"
  config.vm.synced_folder "/Users/ndurell/.ssh", "/home/vagrant/.ssh"
  config.ssh.private_key_path = "/Users/ndurell/.ssh/id_rsa"
  config.vm.provision :shell, :path => "bootstrap.sh"
end
