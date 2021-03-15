Vagrant.configure("2") do |config|
    config.vm.define "rackhd" do |rackhd|    
        rackhd.vm.box = "ubuntu/xenial64"
        rackhd.vm.network "private_network", ip: "172.16.2.2"
        rackhd.vm.hostname = "rackhd"
        rackhd.vm.network "forwarded_port", guest: 8080, host: 8080 
        rackhd.vm.provider "virtualbox" do |vb|
            vb.memory = 4096
        end
    end

	config.vm.define "infra" do |infra|    
        infra.vm.box = "ubuntu/xenial64"
        infra.vm.network "private_network", ip: "172.16.2.4"
        infra.vm.hostname = "infra"
        infra.vm.provider "virtualbox" do |vb|
            vb.memory = 512
        end
    end
end
