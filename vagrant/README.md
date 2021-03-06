## Installation
* Install VirtualBox 4.3.2 ([https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads))
* Install Vagrant 1.3.5 ([http://downloads.vagrantup.com/](http://downloads.vagrantup.com/))

## Setup
* Add the following line to your /etc/hosts:  
  `192.168.33.12 intelmashup.local.sosolimited.com` 
* `cd vagrant`
* Build and provision the vagrant instance: `vagrant up`
* SSH into the instance: `vagrant ssh`


## Notes
* Once the instance is built via `vagrant up`, you'll want to run things from within the vagrant instance, that is, while ssh'ed into the machine via `vagrant ssh` since that's where everything is installed.

* You can, however, edit the files in the project from your host machine in your editor of choice since the project on your host machine is mapped to the vagrant instance at ~/workspace.

* If there are any conflicting services running on your host machine (couchdb, node, nginx, etc.), you'll want to stop them while the vagrant instance is running.

* If you need to restart your host machine you can save the vm state with `vagrant suspend` and restore it with `vagrant resume`

* There are currently some stability issues with VirtualBox in OS X Mavericks. If you get an error when running `vagrant up`, try `sudo /Library/StartupItems/VirtualBox/VirtualBox restart`

## Resources
[Vagrant](http://docs.vagrantup.com/v2/)