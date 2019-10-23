# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  (1..2).each do |i|
    config.vm.define "web#{i}.vagrant.test" do |web|
      web.landrush.enabled = true
      web.vm.hostname = "web#{i}.vagrant.test"
      web.vm.box = "ubuntu/xenial64"
      config.vm.provision "ansible" do |ans|
        ans.playbook = "./ansible/playbook.yml"
      end
    end
  end
end