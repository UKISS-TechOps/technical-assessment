# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
    config.vm.define "technicalAssessment"
    config.vm.box = "boxcutter/centos72"

    # KNOWN ISSUE WITH VAGRANT 1.8.5 - https://github.com/mitchellh/vagrant/issues/7610
    config.ssh.insert_key = false

    config.vm.network :forwarded_port, guest: 80, host: 8000
    config.ssh.forward_agent = true

    config.vm.synced_folder ".", "/var/www/technical-assessment", id: "webroot", :owner => "4665", :group => "4665"

    # ansible_local runs Ansible from inside the Vagrant VM because windows is shit
    config.vm.provision "ansible_local" do |ansible|
        ansible.groups = {
            "local" => ["technicalAssessment"]
        }
        ansible.playbook = "vm/site.yml"
        ansible.provisioning_path = "/var/www/technical-assessment"
    end

    # Vm config
    config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
	    vb.customize ["modifyvm", :id, "--memory", "1048"]
    end
end
