# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|

  config.vm.box       = "centos63-x86"
  config.vm.box_url   = "http://developer.nrel.gov/downloads/vagrant-boxes/CentOS-6.3-i386-v20130101.box"
  config.vm.boot_mode = :gui
  config.vm.host_name = "puppet-primer.localdomain"

  config.vm.customize ["modifyvm", :id, "--memory", 1024]
  config.vm.forward_port 8090, 8090

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.module_path    = "modules"
    puppet.manifest_file  = "primer.pp"
  end
end

