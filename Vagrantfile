Vagrant.configure(2) do |config|
  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "chef/fedora-20"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine.
  # Access AtoM at http://localhost:8080
  config.vm.network "forwarded_port", guest: 80, host: 8080

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", '4096']

    # comment these two lines out if CPU only has one core
    vb.customize ["modifyvm", :id, "--cpus", '2']
    vb.customize ["modifyvm", :id, "--ioapic", "on"]
  end

  # Enabling the Berkshelf plugin
  config.berkshelf.enabled = true

  # Lock Chef version to 12.3.0 to prevent future issues?
  config.omnibus.chef_version = '12.3.0'

  config.vm.provision :chef_solo do |chef|
    chef.add_recipe 'atom'
  end
end
