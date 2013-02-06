puppet-primer
=============

Prerequisites
-------------
Have the following software installed:
* VirtualBox 4.2.x - https://www.virtualbox.org/wiki/Downloads
* Vagrant 1.0.6 - http://downloads.vagrantup.com

Initialization
--------------
Download and add a CentOS 6.3 box for vagrant:

    wget http://developer.nrel.gov/downloads/vagrant-boxes/CentOS-6.3-i386-v20130101.box
    vagrant box add centos63-x86 CentOS-6.3-i386-v20130101.box

Clone puppet-primer git repository:

    git clone https://github.com/xebia/puppet-primer.git

Start the image:

    vagrant up

The following output will be shown when puppet runs successfully:

    [default] Running Puppet with /tmp/vagrant-puppet/manifests/primer.pp...
    notice: Hello
    
    notice: /Stage[main]//Notify[Hello]/message: defined 'message' as 'Hello'
    
    notice: Finished catalog run in 0.03 seconds

Run puppet (again):

    vagrant provision
