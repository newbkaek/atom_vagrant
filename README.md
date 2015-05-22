AtoM Vagrant
=============
This will create a Vagrant environment with [AtoM](https://www.accesstomemory.org/) installed on a CentOS 6.5 box.

This Vagrant configuration uses Chef to provision the VM using [atom_cookbook](https://github.com/newbkaek/atom_cookbook).

Requirements
------------
* [ChefDK](https://downloads.chef.io/chef-dk/)
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://vagrantup.com)
* vagrant-berkshelf plugin
* vagrant-omnibus plugin

## Platform
This Vagrant configuration was developed and tested on Ubuntu 14.04 only

## Usage
1. `git clone https://github.com/newbkaek/atom_vagrant`
2. `cd atom_vagrant`
3. `vagrant install plugin vagrant-berkshelf` (skip if you already have this plugin installed)
4. `vagrant install plugin vagrant-omnibus` (skip if you already have this plugin installed)
5. `vagrant up`
6. Visit http://localhost:8080 on your browser

If you did not change the configuration, this is how you should fill in the fields on the web installer
* Database name: `atom`
* Database username: `atom`
* Database password: `atom`
* Database host: `127.0.0.1`
* Database port: `3306`
* Search host: `127.0.0.1`
* Search port: `9200`
* Search index: `atom`

## Author
* Patrick Fung (<patrick@makestuffdostuff.com>)
