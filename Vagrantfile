Vagrant.configure("2") do |config|
  config.vagrant.plugins = "vagrant-libvirt"
  config.vm.box = "debian/bookworm64"
  config.vm.box_version = "12.20250126.1"
  # no root password, sudo works without password

  # Disable synced folder
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider :libvirt do |libvirt|
    libvirt.memory = 4096
    libvirt.cpus = 4
  end

 config.vm.network :private_network, :ip => "192.168.121.10"
 config.vm.network "forwarded_port", guest: 3000, host: 3000
 config.vm.network "forwarded_port", guest: 9090, host: 9090
 config.vm.network "forwarded_port", guest: 12345, host: 12345

end
