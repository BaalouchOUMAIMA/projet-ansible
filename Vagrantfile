
Vagrant.configure("2") do |config|

  config.vm.box = "bento/ubuntu-22.04"

  # Configuration VMware commune
  config.vm.provider "vmware_desktop" do |vm|
    vm.memory = 2048
    vm.cpus = 2
  end

  # Machine 1 : Ansible Controller
  config.vm.define "ansible-controller" do |controller|
    controller.vm.hostname = "ansible-controller"
    controller.vm.network "private_network", ip: "192.168.100.10"
  end

  # Machine 2 : Web Server
  config.vm.define "web-server" do |web|
    web.vm.hostname = "web-server"
    web.vm.network "private_network", ip: "192.168.100.11"
  end

end
