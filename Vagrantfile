# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.box = "centos6.7"
  config.vm.network "forwarded_port", guest: 3306, host: 3306
  config.vm.network "forwarded_port", guest: 80, host: 8888
  config.vm.synced_folder "../server", "/var/www/server", owner: "vagrant", group: "vagrant", mount_options: ["dmode=777","fmode=777"]
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "../ansible/site.yml"
    ansible.inventory_path = "../ansible/hosts/local"
    ansible.limit = 'all'
    ansible.raw_arguments = ["--diff"]
  end
end
