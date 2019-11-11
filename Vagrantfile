# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  (1..1).each do |i|
    config.vm.define "web#{i}.vagrant.test" do |web|
      web.landrush.enabled = true
      web.vm.hostname = "web#{i}.vagrant.test"
      web.vm.box = "centos/7"
      # web.vm.network "forwarded_port", guest: 8080, host: "1008#{i}"
    end
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "./ansible/playbook.yml"
  end

end
