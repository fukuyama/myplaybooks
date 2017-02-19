# -*- mode: ruby -*-
# vi: set ft=ruby :

# vagrant plugin install vagrant-vbguest

# http://qiita.com/ozawan/items/9751dcfd9bd4c470cd82

Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"

  # http://qiita.com/tenmyo/items/c2bb714117c98ae979de
  config.vm.synced_folder ".", "/vagrant", type: "virtualbox"

  # config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vb|
    vb.gui    = true
    vb.memory = "1024"
  end

  config.vm.provision "shell", inline: <<-SHELL
    rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
    yum install -y ansible
  SHELL

end
