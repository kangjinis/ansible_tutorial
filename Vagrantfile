# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "web0.vagrant.test" do |web|
    web.landrush.enabled = true
    web.vm.hostname = 'web0.vagrant.test'
    web.vm.box = "ubuntu/xenial64"
    config.vm.provision "ansible" do |ans|
      ans.playbook = "./ansible/playbook.yml"
    end
  end
end

  # (1..2).each do |i|
  #   config.vm.define "web#{i}.kangjin" do |subconfig|
  #     subconfig.dns.tld = "test"
  #     subconfig.vm.hostname = "vagrant"
  #     subconfig.dns.patterns = "web#{i}.kangjin.test"
  #     subconfig.vm.box = box
  #     subconfig.vm.network "private_network", ip: "10.240.0.#{i+15}"
  #     # subconfig.vm.provision 'ansible' do |ans|
  #     #   ans.playbook = "./ansible/playbook.yml"
  #     # end
  #   end
  # end

  # config.vm.define "web0" do |web|
  #   web.vm.box = box
  #   web.vm.hostname = 'web0'
  #   config.vm.provision "ansible" do |ans|
  #     ans.playbook = "./ansible/playbook.yml"
  #   end
  # end

  # config.vm.define "web1" do |web|
  #   web.vm.box = box
  #   web.vm.hostname = 'web0'
  #   config.vm.provision "ansible" do |ans|
  #     ans.playbook = "./ansible/playbook.yml"
  #   end
  # end