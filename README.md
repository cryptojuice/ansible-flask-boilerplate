*Bootstrap for Flask development enviornment.

**Includes:
Web server: Flask, Nginx, Gunicorn, Gevent
DB server: MongoDB

Usage:

Install VirtualBox, Vagrant, and Ansible on local machine.

From shell run commands
vagrant box add precise32 http://files.vagrantup.com/precise32.box
vagrant box add precise64 http://files.vagrantup.com/precise64.box

git clone ansible-flask-boostrap into folder

From shell run command:
vagrant up web && vagrant up db 
vagrant provision
