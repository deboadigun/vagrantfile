# -*- mode: ruby -*- 
# vi: set ft=ruby : 
VAGRANTFILE_API_VERSION = "2" 
Vagrant.configure(VAGRANTFILE_API_VERSION) do|config| 
    config.ssh.insert_key = false 
    config.vm.provider :virtualbox do|vb| 
        vb.customize ["modifyvm", :id, "--memory", "512"] 
    end 

    #Ansible Server 
    config.vm.define "ans" do|ans| 
        ans.vm.hostname = "master" 
        ans.vm.box = "geerlingguy/centos7" 
        ans.vm.network "private_network", ip: "192.168.43.11" 
    end     

    #Web Server 
    config.vm.define "web" do|web| 
        web.vm.hostname = "webserver" 
        web.vm.box = "geerlingguy/centos7" 
        web.vm.network "private_network", ip: "192.168.43.12" 
    end 
    
    #Application Server1 
    config.vm.define "app" do|app| 
        app.vm.hostname = "appserver" 
        app.vm.box = "geerlingguy/centos7" 
        app.vm.network "private_network", ip: "192.168.43.13" 
    end 
    
    
    #Database Server 
    config.vm.define "db" do|db| 
        db.vm.hostname = "database" 
        db.vm.box = "geerlingguy/centos7" 
        db.vm.network "private_network", ip: "192.168.43.14" 
    end 
    
#    config.vm.box_check_update = false 
#    config.vbguest.auto_update = false 
end
