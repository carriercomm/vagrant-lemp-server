Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu-precise12042-x64-vbox43"
  config.vm.box_url = "http://box.puphpet.com/ubuntu-precise12042-x64-vbox43.box"

  config.vm.network "private_network", ip: "192.168.10.10"


  config.vm.synced_folder "/usr/local/vagrant-lemp-server/www", "/var/www", id: "vagrant-root", :nfs => false

  config.vm.usable_port_range = (2200..2250)
  config.vm.provider :virtualbox do |virtualbox|
    virtualbox.customize ["modifyvm", :id, "--name", "lemp-server"]
    virtualbox.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    virtualbox.customize ["modifyvm", :id, "--memory", "512"]
    virtualbox.customize ["setextradata", :id, "--VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root", "1"]
  end

  config.ssh.username = "vagrant"

  config.ssh.shell = "bash -l"

  config.ssh.keep_alive = true
  config.ssh.forward_agent = false
  config.ssh.forward_x11 = false
  config.vagrant.host = :detect
end

