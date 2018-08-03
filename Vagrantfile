# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "minimal/xenial64"
  config.vm.define "vagrant_mediawiki"
  config.vm.hostname = "mediawiki.rnjudas.local"
  config.vm.network "private_network", ip: "192.168.34.8"
   config.vm.provider "virtualbox" do |vb|
	vb.gui = true
	vb.name = "Vagrant MediaWiki"
     vb.memory = "1024"
  config.vm.synced_folder "./src", "/srv/project"
   end
  config.vm.provision "shell", inline: <<-SHELL
  #Update the repos
  apt-get update
  #Install Git
  sudo apt-get install git-core -y
  #Install Ansible to the local system
  sudo apt-get install software-properties-common -y
  sudo apt-add-repository ppa:ansible/ansible
  sudo apt-get update
  sudo apt-get install ansible -y
  ssh-keygen -t rsa -N '' -f /root/.ssh/id_rsa -q
  cat /root/.ssh/id_rsa.pub >> /home/vagrant/.ssh/authorized_keys
  export ANSIBLE_HOST_KEY_CHECKING=False
  export MWHOME=/var/lib/mediawiki
  ansible-playbook -i 'localhost,' /srv/project/playme/play.yml -e "ROLE=cat-mwa" -e "USER=vagrant" -e "HOSTNAME=localhost"
  SHELL
end
