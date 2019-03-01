
# The contents below were provided by the Packer Vagrant post-processor

Vagrant.configure("2") do |config|
  config.vm.base_mac = "080027D59D5A"
end


# The contents below (if any) are custom contents provided by the
# Packer template during image build.
# -*- mode: ruby -*-
# vi: set ft=ruby :

current_version = Gem::Version.new(Vagrant::VERSION)
windows_version = Gem::Version.new("1.6.0")

Vagrant.configure("2") do |config|
    config.vm.define "vagrant-windows-2012-r2"
    config.vm.box = "windows_2012_r2"

    if current_version < windows_version
      if !Vagrant.has_plugin?('vagrant-windows')
        puts "vagrant-windows missing, please install the vagrant-windows plugin!"
        puts "Run this command in your terminal:"
        puts "vagrant plugin install vagrant-windows"
        exit 1
      end

      # Admin user name and password
      config.winrm.username = "vagrant"
      config.winrm.password = "vagrant"

      config.vm.guest = :windows
      config.windows.halt_timeout = 15

      # Port forward WinRM and RDP
      config.vm.network :forwarded_port, guest: 5985, host: 5985, id: "winrm", auto_correct: true
      config.vm.network :forwarded_port, guest: 3389, host: 3389
    else
      config.vm.communicator = "winrm"
    end

    config.vm.provider :virtualbox do |v, override|
        v.customize ["modifyvm", :id, "--memory", 2048]
        v.customize ["modifyvm", :id, "--cpus", 2]
    end
end

