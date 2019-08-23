# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  
  config.vm.provision :chef_solo do |chef|
    chef.custom_config_path = "terra-chef/CustomConfiguration.chef"
    chef.cookbooks_path = "terra-chef/cookbooks"
	chef.roles_path = "terra-chef/roles"
	chef.add_role "mail_filter"
  end
end
