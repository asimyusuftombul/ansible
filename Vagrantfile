$script = <<-SCRIPT
sed -i "s/.*PasswordAuthentication.*/PasswordAuthentication yes/g" /etc/ssh/sshd_config
systemctl restart sshd
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: $script

  config.vm.define "ozan" do |node|
    node.vm.box = "ubuntu/focal64"
    node.vm.network "private_network", ip: "192.168.56.10"
  end

  config.vm.define "yusuf" do |node|
    node.vm.box = "ubuntu/focal64"
    node.vm.network "private_network", ip: "192.168.56.11"
  end
 

  config.vm.define "gulay" do |node|
    node.vm.box = "ubuntu/focal64"
    node.vm.network "private_network", ip: "192.168.56.12"
  end
 
  config.vm.define "seyma" do |node|
    node.vm.box = "ubuntu/focal64"
    node.vm.network "private_network", ip: "192.168.56.13" 
  end

end

