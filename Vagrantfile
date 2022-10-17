Vagrant.configure("2") do |config|
  config.vm.define "master" do |ubuntu|
  ubuntu.vm.box = "hashicorp/bionic64"
  ubuntu.vm.network "forwarded_port", guest: 80, host: 3002, host_ip: "127.0.0.1"
  ubuntu.vm.network "public_network", bridge: "Realtek Gaming GbE Family Controller", ip: "192.168.1.20"
  ubuntu.vm.provision "shell", inline: "sudo apt update -y"
  ubuntu.vm.provision "shell", inline: "sudo apt install python3"
  ubuntu.vm.provision "shell", inline: "sudo apt install python-is-python3 -y"
  ubuntu.vm.provision "shell", inline: "sudo apt install python3-pip -y"
  ubuntu.vm.provision "shell", inline: "sudo python -m pip install --upgrade pip"
  ubuntu.vm.provision "shell", inline: "sudo pip install ansible==2.9.10"
  ubuntu.vm.provider "virtualbox" do |vb|
    vb.name = "master"
    vb.gui = true
    vb.memory = "1024"
    vb.cpus = "2"
  end

  config.vm.define "maquina1" do |debian|
  debian.vm.box = "debian/buster64"
  debian.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  debian.vm.network "public_network", bridge: "Realtek Gaming GbE Family Controller", ip: "192.168.1.21"
  debian.vm.provision "shell", inline: "sudo apt update -y"
  debian.vm.provision "shell", inline: "sudo apt install python3"
  debian.vm.provision "shell", inline: "sudo apt install python-is-python3 -y"
  debian.vm.provision "shell", inline: "sudo apt install python3-pip -y"
  debian.vm.provision "shell", inline: "sudo python -m pip install --upgrade pip"
  debian.vm.provider "virtualbox" do |vb|
    vb.name = "maquina1"
    vb.gui = true
    vb.memory = "1024"
    vb.cpus = "2"
  end

    
  config.vm.define "maquina2" do |debian|
  debian.vm.box = "debian/buster64"
  debian.vm.network "forwarded_port", guest: 80, host: 8888, host_ip: "127.0.0.1"
  debian.vm.network "public_network", bridge: "Realtek Gaming GbE Family Controller", ip: "192.168.1.22"
  debian.vm.provision "shell", inline: "sudo apt update -y"
  debian.vm.provision "shell", inline: "sudo apt install python3"
  debian.vm.provision "shell", inline: "sudo apt install python-is-python3 -y"
  debian.vm.provision "shell", inline: "sudo apt install python3-pip -y"
  debian.vm.provision "shell", inline: "sudo python -m pip install --upgrade pip"
  debian.vm.provider "virtualbox" do |vb|
    vb.name = "maquina2"
    vb.gui = true
    vb.memory = "1024"
    vb.cpus = "2"
  end
end
