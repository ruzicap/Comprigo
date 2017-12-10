# Comprigo
Assignment


#####  I got following assignment for job qualification:
====================
###### Create a repository on BitBucket or GitHub with the following:

- A Vagrantfile for managing a VM with a Linux-based OS of your choice. Use a publicly available box.
- A provisioner (Ansible, Chef, Puppet, Salt) to manage the configuration of the services in the Vagrantfile.
###### Provisioned services:
- HAProxy
    * Configure SSL termination on frontend
    * Create a self-signed certificate or use LetsEncrypt, also document the commands you are using to create the certificate
    * Use TLS only
  	* Use strong ciphers only
  	* Generate a DH key and enable dhparam, also document the commands you are using to create a dh key
  	* Enable HSTS
  	* Enable OCSP Stapling
  	* Send traffic to nginx SSL backend
- nginx
  	* Enable HTTPS
  	* Enable Nginx Microcaching and make sure Cache is not enabled in Admin Area and for logged in users
  	* Add any other configuration you may think is important (headers, deny access to important files and folders, ...)
- php-fpm
  	* For process management: choose either static, on demand, dynamic, also explain your decision
  	* Listen directive: choose either Socket or TCP, also explain your decision
  	* Add any other configuration you may think is important (number of workers, timeout, …)
- Redis
  	* Create a Timer Unit File to execute a self written script by yourself (bash, python, ..) every 5 minutes to load some dummy data into Redis (can be simple key/value i.e. hello/world)
- MySQL
 	 * Create a simple website to serve with php-fpm that displays the string 'Hello World'
###### Write your explanations and documentations into the Readme
====================

My local station runs following distribution: Ubuntu 16.04.2 LTS.

Firstly, I needed to set up tools for this assignment since my locl station is new. I was missing VirtualBox, Vagrant and Ansible.

Here are the official links on HowTo so I do not end up making this longer than needed:
- https://www.virtualbox.org/wiki/Linux_Downloads
- https://www.vagrantup.com/docs/installation/
- http://docs.ansible.com/ansible/latest/intro_installation.html#installing-the-control-machine

Now that I had everything, I had to set up Vagrant file that would load my VirtualBox. I am choosing CentOS 7 here, as I use it more than Ubuntu or any other distribution.
