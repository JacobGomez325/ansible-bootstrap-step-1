Vagrant.configure("2") do |config|

  numberServer = 3 
  (1..numberServer).each do |i|
    config.vm.define "server-#{i}" do |node|
      config.vm.box = "debian/buster64"
      node.vm.hostname = "server-#{i}"
      node.vm.network :private_network, ip: "192.168.56.15#{i}"
      config.vm.provision "file", source: "./id_rsa.pub", destination: "~/.ssh/id_rsa.pub"

    end
  end
 
end



