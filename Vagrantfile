# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.define "testvm"  do  |machine|
        machine.vm.box = "ubuntu/trusty64"
        machine.vm.network :private_network, ip: "192.168.33.21"

        machine.vm.provision "ansible" do |ansible|
            ansible.playbook = "provisioning/playbook.yml"
            ansible.limit = 'all'
            ansible.verbose = "vvv"
            ansible.sudo = "true"
        end
        
        machine.vm.provider "virtualbox" do |v|
        # Use VBoxManage to customize the VM. For example to change memory:
            v.customize ["modifyvm", :id, "--memory", "1024"]
            v.customize ["modifyvm", :id, "--cpuexecutioncap", "95"]
        end
    end
end

