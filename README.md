# Description

Since ansible does not use any agent software, I wrote a tool to bring a targeted
node under control.

# Requirements

 - Ansible is installed on a box you wish to bootstrap from.

 - shc is installed on your ansible box. (See notes for ansible playbook) 

# Instructions

 - Copy src/*.example files without the .example extension and mofidy as needed.
    Change the LOCAL_SUBNET and SSH_RSA

 - Change the USERNAME in scripts/install-bootstrap

 - Run ./scripts/make-bootstrap-executable to generate obfuscated script executables

 - Run ./scripts/install-bootstrap CURRENT_IP DESIRED_IP

  For example if the machine you want to control is at 192.168.1.100 but you want it to be
  192.168.1.200  ./scripts/install-bootstrap 192.168.1.100 192.168.1.200

# Security
 - I can not gaurantee this is the most secure method, use at your own risk!

# Notes

 - Do not try to run the scripts in the src file, they will self destruct!

 - I have created an ansible playbook to automate installation, but it is a pretty 
  straight forward make install. (https://github.com/jgrowl/ansible-playbook-shc)

 - If there is a better way to do this, please let me know!

# TODO

 - Externalize a number of things including the network configuration and the USERNAME in the install-bootstrap script
