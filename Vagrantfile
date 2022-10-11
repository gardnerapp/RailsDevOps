Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
  config.vm.hostname = "rails"

  # Forward boxes http port to local_host:8080
  config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # private network with host only access
  config.vm.network "private_network", type: "dhcp"

  # virtualbox configurations
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.name = "rails_box"
    vb.customize ["modifyvm", :id, "--uart1", "0x3F8", "4"]
    vb.customize ["modifyvm", :id, "--uartmode1", "file", File::NULL]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "./ansible/rails.yml"
    ansible_compatibility_mode = "2.0"
  end
end
