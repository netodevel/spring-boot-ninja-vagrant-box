# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    config.vm.define "testvm"  do  |testvm|
        testvm.vm.box = "ubuntu/trusty64"
        testvm.vm.network :private_network, ip: "192.168.33.21"

        testvm.vm.provision "ansible" do  |ansible|
            ansible.playbook  = "webserver.yml"
            ansible.verbose = "vvv"
        end
    end

    config.vm.provider  "virtualbox"  do  |v|
        v.customize ["modifyvm",  :id,  "--memory", "1024"]
    end
  
end
