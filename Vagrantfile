Vagrant.configure("2") do |config|
  config.vagrant.plugins = "vagrant-libvirt"
  config.vm.box = "generic/debian12"
  config.vm.box_version = "4.3.12"


  config.vm.provider :libvirt do |libvirt|
    libvirt.memory = 4096
    libvirt.cpus = 4
  end

 config.vm.network :private_network, :ip => "192.168.121.10"
 config.vm.network "forwarded_port", guest: 3000, host: 3000

end
