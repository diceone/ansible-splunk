# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "c65"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "http://vntx.cc/boxes/centos65.box"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  config.vm.network :forwarded_port, guest: 8000, host: 8000

  config.vm.provider :virtualbox do |vb|
    vb.gui = false
  end

  # provision with ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook          = "playbook.yaml"
    ansible.sudo              = true
    ansible.host_key_checking = false
  end
end
