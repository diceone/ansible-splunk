# Vagrant Box (CentOS 6.5) with Splunk install via Ansible

Installs and sets running Splunk, on top of a [@core CentOS6 Vagrant
Box](http://vntx.cc/boxes/centos65.box).

Tested with CentOS 6.5 64bit and splunk-6.1.1-207789-linux-2.6-x86_64.rpm

You need ansible.
Redhat:
yum install ansible
Debian:
apt-get install ansible
MacOSX:
brew install ansible

You need Virtualbox and Vagrant (www.vagrantup.com)

Download latest Splunk rpm and put it in /sw/splunk-6.1.1-207789-linux-2.6-x86_64.rpm

Check it's the same version as mentioned in
playbook.yaml
and adjust the filename accordingly if it's not.

If you have everything installed and in the right place just start the
vagrant box vom base dir with "vagrant up"

The VM will boot and install Splunk and set it running. You
can browse to http://localhost:8000 on your host machine to log in.
