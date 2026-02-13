Vagrant.configure("2") do |config|

  # Configuration du Serveur (SRVADVAR01)
  config.vm.define "server" do |server|
    server.vm.box = "opentable/win-2019-standard-amd64-nocm" # Image légère de Win Server 2019
    server.vm.hostname = "SRVADVAR01"
    
    # Configuration Réseau Privé (IP Statique)
    server.vm.network "private_network", ip: "192.168.88.5"
    
    server.vm.provider "virtualbox" do |vb|
      vb.memory = "3072"
      vb.cpus = 2
      vb.gui = true # On active l'interface graphique pour tes manips
    end
  end

  # Configuration du Client (WIN01)
  config.vm.define "client" do |client|
    client.vm.box = "jordansissel/windows-10" # Image Windows 10
    client.vm.hostname = "WIN01"
    
    client.vm.network "private_network", ip: "192.168.88.10"
    
    client.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.gui = true
    end
  end
end
