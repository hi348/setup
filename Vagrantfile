Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.define "nyu-network-class" do |dev_machine|
    # config.vm.network "forwarded_port", guest: 2020, host: 2020
    dev_machine.vm.provider "virtualbox" do |v|
      v.name = "nyu-network-class"
      v.memory = 2048
      v.cpus = 2
    end
    dev_machine.vm.provision :docker

    # Install Python related stuff
    dev_machine.vm.provision "python", type: "shell", inline: <<-EOC
      sudo apt-get install -y python-pip python-dev build-essential
      sudo pip install virtualenv
      sudo pip install --upgrade pip
    EOC
  end
end
