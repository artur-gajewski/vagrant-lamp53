Vagrant setup for Linux, Apache2, MySQL and PHP 5.4  
===================================================

Welcome to the repository for Vagrant skeleton package. This skeleton is the starting point for building your development environment in a virtual server.


###Features

This skeleton features Linux (CentOS 6.2 64bit version), PHP 5.3, MySQL and Apache2 with xDebug and PhpMyAdmin.

In many situations, you are all set with starting development, but in some cases you might need to add modules to this setup.


###Vagrant/Puppet Installation

To get up and running you need the following installed on your machine:

* [Ruby](http://www.ruby-lang.org/en/downloads/)
* [Vagrant](http://downloads.vagrantup.com/)
* [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads)

To check if you already have Ruby installed, you can enter this at the command line:

	$ ruby -v


###Creating development environment

Once you have the required software installed, and you have cloned your fork to your computer, navigate to the project's root directory and run the following CLI command:

	$ vagrant up
	
That's it! I know, it's too easy. The first time you run this command, it may take a few minutes to complete. Subsequent invocations should run much faster.  A VirtualBox window will open and multiple lines of output will appear inside it and at the command line. When it is finished, you will be returned to the command prompt and you can minimise the VirtualBox window out of view.

Congratulations, you now have a fully functional project development environment!


###Development folder

The folder you run the vagrant command from is your project's root.

Initially you should see Apache 2 Test Page. Once you place index.php into that folder, that file will be loaded.

If you need to SSH to the vagrant's server instance use

    $ vagrant ssh

The root of the server is located in /vagrant folder, which is the same as the folder you ran vagrant from.


####URLs

You can view the project or use PHPMyAdmin in your browser using the following:

	http://33.33.33.10
	http://33.33.33.10/phpmyadmin 


####Essential Vagrant Commands

Run this command before closing the VBox window, or shutting down your computer:

	$ vagrant suspend
	
This starts the process again:

	$ vagrant resume
	
Run this to destroy the VirtualBox (removing the development environment completely from your machine):

	$ vagrant destroy
	
This creates a new VirtualBox (use this if you destroyed a previous installation):

	$ vagrant up
	
The following command is a housekeeping action which you shouldn't need to worry about, but its here if you want it:

	$ vagrant provision


####Further Reading

If you would like to know more about how this skeleton was set up, [read Joshua's informative blog post](http://www.adayinthelifeof.nl/2012/06/29/using-vagrant-and-puppet-to-setup-your-symfony2-environment/).
