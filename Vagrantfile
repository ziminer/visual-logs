# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

# Comment out this line if you want to use VirtualBox
ENV['VAGRANT_DEFAULT_PROVIDER'] = 'vmware_fusion'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible-playbook/logvisualization.yml"
  end

  config.vm.network "private_network", type: :dhcp
end
