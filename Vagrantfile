Vagrant.configure("2") do |config|

  config.vm.define "teste1" do |teste1|
    teste1.vm.box = "ubuntu/xenial64"
    teste1.vm.network "public_network",  bridge: "wlp4s0"
    config.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
    config.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y htop
    SHELL
  end

end
