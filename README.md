#Flask development enviornment.

####Includes
**Web server:** Flask, Nginx, Gunicorn, Gevent  
**DB server:** MongoDB

####Required
VirtualBox or VMware, Vagrant, and Ansible installed on local machine.

####Usage

**1. Add vm's to vagrant**  
vagrant box add precise32 http://files.vagrantup.com/precise32.box
vagrant box add precise64 http://files.vagrantup.com/precise64.box

**2. Create new project dir**   
git clone ansible-flask-boostrap into new directory.

**3. Run shell commands**  
\:# vagrant up web && vagrant up db   
\:# vagrant provision
