# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.define "user" do |u|
    u.vm.network "private_network", ip: "192.168.50.5"

    config.vm.provider "virtualbox" do |v|
      v.name = "user"
    end
    config.vm.hostname = "user"
  end

  config.vm.define "proxy" do |p|
    p.vm.network "private_network", ip: "192.168.50.6"

    config.vm.provider "virtualbox" do |v|
      v.name = "proxy"
    end
    config.vm.hostname = "proxy"
  end

  config.vm.define "dns1" do |d|
    d.vm.network "private_network", ip: "192.168.60.8"

    config.vm.provider "virtualbox" do |v|
      v.name = "dns1"
    end
    config.vm.hostname = "test.fl1"
  end

  config.vm.define "dns2" do |d|
    d.vm.network "private_network", ip: "192.168.70.8"

    config.vm.provider "virtualbox" do |v|
      v.name = "dns2"
    end
    config.vm.hostname = "test.fl2"
  end

  config.vm.define "d1web" do |d|
    d.vm.network "private_network", ip: "192.168.60.5"

    config.vm.provider "virtualbox" do |v|
      v.name = "d1web"
    end
    config.vm.hostname = "web.test.fl1"
  end

  config.vm.define "d1db" do |d|
    d.vm.network "private_network", ip: "192.168.60.7"

    config.vm.provider "virtualbox" do |v|
      v.name = "d1db"
    end
    config.vm.hostname = "db.test.fl1"
  end

  config.vm.define "d2web" do |d|
    d.vm.network "private_network", ip: "192.168.70.5"

    config.vm.provider "virtualbox" do |v|
      v.name = "d2web"
    end
    config.vm.hostname = "web.test.fl2"
  end

  config.vm.define "d2db" do |d|
    d.vm.network "private_network", ip: "192.168.70.7"

    config.vm.provider "virtualbox" do |v|
      v.name = "d2db"
    end
    config.vm.hostname = "db.test.fl2"
  end

end
