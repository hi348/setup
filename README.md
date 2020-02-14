# Instructions for setting up your local development environment

- Install Virtualbox: https://www.virtualbox.org
- Install Vagrant: https://www.vagrantup.com
- Make sure that both virtualbox and vagrant are available from your shell.
    - Try `vboxmanage` for Virtualbox in the shell
    - Try `vagrant` for Vagrant in the shell
    - Both commands should return some output, detailing how to use the commands.
    - If above commands do not work, or not recognized in your shell, make sure to include them in your path. For example, in windows (make sure that the path for the virtualbox/vagrant is correct): `set PATH=%PATH%;"C:\Program Files\Oracle\VirtualBox"`
- Once both Virtualbox and Vagrant are successfully installed and available from your shells.
    - Create a folder, and name to your choice.
    - Copy the `Vagrantfile` provided in this repository to the folder.
    - Execute `vagrant up`. This will download and run an Ubuntu machine and install docker and python for you.
    - Once done, execute `vagrant ssh` to login to your machine.
    - Once logged in go to `cd /vagrant`. This directory will be synced with your host machine. Therefore you can put any file in here in your host machine and it will be visible to your Ubuntu machine. 
    - At this step you should have a ubuntu box in your host machine that you can use for development. To learn more about vagrant, please see the documentation.
