Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.synced_folder ".", "/vagrant", disabled: true
    config.vm.define "Ubuntu" do |server|
        server.vm.provision "Install bcc from source", type: "shell", privileged:true, path: "bcc"
        server.vm.provider "virtualbox" do |vb|
            vb.memory = 4096
            vb.cpus = 2
        end
        server.vm.network "public_network", ip: "192.168.0.10"
    end
end
