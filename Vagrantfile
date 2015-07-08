# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define :trusty64 do |trusty64|
    trusty64.vm.box = "ubuntu/trusty64"
    trusty64.vm.hostname = 'trusty64'
    trusty64.vm.network "private_network", ip: "192.168.33.10"

    trusty64.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "2"]
    end
  end

  config.vm.define :centos7 do |centos7|
    centos7.vm.box = "puppetlabs/centos-7.0-64-puppet"
    centos7.vm.hostname = 'centos7'
    centos7.vm.network "private_network", ip: "192.168.33.11"

    centos7.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "2"]
    end
  end


end
