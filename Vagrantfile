Vagrant.configure("2") do |config|


    config.vm.provider "virtualbox" do |v|
        v.memory = 1024
        v.cpus = 2
    end
  

    config.vm.define "admin" do |admin|
        admin.vm.box = "bento/ubuntu-22.04"
        admin.vm.synced_folder ".", "/vagrant", disabled: true
        admin.vm.synced_folder "./configs", "/configs" 
        admin.vm.provision "shell", inline: "sh /configs/script-admin.sh"
        #admin.vm.network "forwarded_port", guest: 80, host: 8080 
        #admin.vm.network "public_network", ip: "192.168.15.100"
        admin.vm.network "private_network", ip: "192.168.56.0", adress: "255.255.255.0"

       
    end

    #config.vm.define "no1" do |no1|
     #   no1.vm.box = "bento/ubuntu-22.04"
      #  no1.vm.synced_folder ".", "/vagrant", disabled: true
       # no1.vm.synced_folder "./configs", "/configs"
       #no1.vm.provision "shell", inline: "sh /configs/script-no.sh"
       # no1.vm.network "public_network", ip: "192.168.15.101"
    #end

    #config.vm.define "no2" do |no2|
       # no2.vm.box = "bento/ubuntu-22.04"
       # no2.vm.synced_folder ".", "/vagrant", disabled: true
       # no2.vm.synced_folder "./configs", "/configs"
      #   no2.vm.network "public_network", ip: "192.168.15.102"
    #end

    #config.vm.define "no3" do |no3|
        #no3.vm.box = "bento/ubuntu-22.04"
        # no3.vm.synced_folder "./configs", "/configs"
      #  no3.vm.provision "shell", inline: "sh /configs/script-no.sh"
      #  no3.vm.network "public_network", ip: "192.168.15.103"
    #end

end


