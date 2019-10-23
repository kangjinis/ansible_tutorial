# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  (1..2).each do |i|
    config.vm.define "web#{i}.vagrant.test" do |web|
      web.landrush.enabled = true
      web.vm.hostname = "web#{i}.vagrant.test"
      web.vm.box = "centos/7"
    end
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "./ansible/playbook.yml"
  end
end