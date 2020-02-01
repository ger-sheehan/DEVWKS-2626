# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  config.vm.define "n9kv1" do |n9kv1|

        n9kv1.vm.box = "9.3.3"

        n9kv1.ssh.insert_key = false
        n9kv1.vm.boot_timeout = 600
        n9kv1.ssh.shell = "run bash"

        if Vagrant.has_plugin?("vagrant-vbguest")
          config.vbguest.auto_update = false
        end

        config.vm.synced_folder ".", "/vagrant", disabled: true

        config.vm.box_check_update = false
        n9kv1.vm.provision "ansible" do |ansible|
          #ansible.become = true
          #ansible.verbose = true
          #ansible.gather_facts = false
          #ansible.become_user = "root"
          ansible.playbook = "n9kv1.yml"
          ansible.compatibility_mode = "2.0"
        end
        #n9kv1.vm.synced_folder './certs', '/bootflash/home/vagrant/certs'
        #n9kv1.vm.network :forwarded_port, guest: 80, host: 10001
        #n9kv1.vm.network :forwarded_port, guest: 22, host: 1022
        #n9kv1.vm.network :forwarded_port, guest: 50051, host: 50051


        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "bird1-to-n9kv"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "bird2-to-n9kv"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "TICK-to-n9kv"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "nxosv_network4"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "nxosv_network5"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "nxosv_network6"

        #n9kv.vm.network "private_network", auto_config: false, virtualbox__intnet: "nxosv_network7"

        n9kv1.vm.provider :virtualbox do |vb|

                vb.customize [ "guestproperty", "set", :id, "/VirtualBox/GuestAdd/VBoxService/--timesync-set-threshold", 1000 ]
                vb.customize ['modifyvm',:id,'--nicpromisc2','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc3','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc4','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc5','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc6','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc7','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc8','allow-all']
        end
      end
    config.vm.define "n9kv2" do |n9kv2|

        n9kv2.vm.box = "9.3.3"

        n9kv2.ssh.insert_key = false
        n9kv2.vm.boot_timeout = 600
        n9kv2.ssh.shell = "run bash"

        if Vagrant.has_plugin?("vagrant-vbguest")
          config.vbguest.auto_update = false
        end

        config.vm.synced_folder ".", "/vagrant", disabled: true

        config.vm.box_check_update = false
        n9kv2.vm.provision "ansible" do |ansible|
          #ansible.become = true
          #ansible.verbose = true
          #ansible.gather_facts = false
          #ansible.become_user = "root"
          ansible.playbook = "n9kv2.yml"
          ansible.compatibility_mode = "2.0"
        end
        #n9kv1.vm.synced_folder './certs', '/bootflash/home/vagrant/certs'
        #n9kv1.vm.network :forwarded_port, guest: 80, host: 10001
        #n9kv1.vm.network :forwarded_port, guest: 22, host: 1022
        #n9kv1.vm.network :forwarded_port, guest: 50051, host: 50051


        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "bird1-to-n9kv"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "bird2-to-n9kv"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "TICK-to-n9kv"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "nxosv_network4"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "nxosv_network5"

        #n9kv1.vm.network "private_network", auto_config: false, virtualbox__intnet: "nxosv_network6"

        #n9kv.vm.network "private_network", auto_config: false, virtualbox__intnet: "nxosv_network7"

        n9kv2.vm.provider :virtualbox do |vb|

                vb.customize [ "guestproperty", "set", :id, "/VirtualBox/GuestAdd/VBoxService/--timesync-set-threshold", 1000 ]
                vb.customize ['modifyvm',:id,'--nicpromisc2','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc3','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc4','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc5','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc6','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc7','allow-all']
                vb.customize ['modifyvm',:id,'--nicpromisc8','allow-all']

        end
      end
end
