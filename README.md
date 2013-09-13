# [LEMP](http://library.linode.com/lemp-guides) provisioned by chef-solo on Vagrant

* [Vagrant](http://vagrantup.com)
* [Nginx](http://wiki.nginx.org/Main)
* PHP-FPM (with APC, CURL, GD, MySQL modules)
* PHP Extras (Xdebug and PHPUnit)
* MySQL
* [Cakephp Framework](http://cakephp.org/)

Vagrant is a tool for building and distributing virtualized development environments.

By providing automated creation and provisioning of virtual machines using [Oracle’s VirtualBox](http://www.virtualbox.org),
Vagrant provides the tools to create and configure lightweight, reproducible, and portable
virtual environments. For more information, see the part of the getting started guide
on [Why Vagrant?](http://vagrantup.com/v1/docs/getting-started/why.html)

## Quick Start

First, make sure your development machine has [VirtualBox](http://www.virtualbox.org)
installed (version 4.2 and later are preferable). The setup from that point forward is very easy:

	1. Install Vagrant (version 1.0.5 and later are preferable)
	2. $ git clone --recursive https://github.com/gustavobgama/LEMP-Box.git your-folder
	3. cd your-folder
	4. $ git checkout cake
	5. $ git submodule init
	6. $ git submodule update
	7. $ vagrant up
	8. Wait a few minutes
	9. $ sudo su and then # echo "10.10.10.11  cake.dev" >> /etc/hosts

## Results

* NGINX + PHP responding on IP 10.10.10.11 (in browser, type http://cake.dev and see a default Cake installation)
* Xdebug ready for NetBeans depuration
* MySQL connection available form host machine (*Host*: 10.10.10.11, *User*: root, *Password*: password)

##  Known Issues

* In first time you are running the command *vagrant up*, is possible that vagrant will return the following message: "VM must be created before running this command. Run `vagrant up` first." In this case you only need reload the configuration with this command: *vagrant reload*.
