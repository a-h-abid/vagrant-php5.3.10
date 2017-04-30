# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "ubuntu/precise64"

    config.vm.network :private_network, ip: "192.168.10.53"
    config.vm.network :forwarded_port, guest: 80, host: 8053

    config.vm.provision :shell, :path => "install.sh"

    config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777", "fmode=666"]

    # If true, then any SSH connections made will enable agent forwarding.
    # Default value: false
    # config.ssh.forward_agent = true

    # Share an additional folder to the guest VM. The first argument is
    # the path on the host to the actual folder. The second argument is
    # the path on the guest to mount the folder. And the optional third
    # argument is a set of non-required options.
    ###
    # IMPORTANT
    ###
    # Before you boot up this machine set the first argument "D:/abid/php/" to you html pulbic path
    config.vm.synced_folder "D:/abid/php/", "/var/www/html"
end
