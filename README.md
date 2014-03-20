Overview
--------
vxlan-gateway charm copies Nexus 1000V virtual machine image
into the glance image store. 

vxlan-gateway charm is designed as a subordinate charm under 
primary nova-cloud-controller charm.


Usage
-----
In order to use Cisco Nexus 1000V VXLAN Gateway administrator
needis to first install VXLAN GATEWAY Debian package to the 
glance node from where its virtual machine image can be extracted
onto a predefined file repository for later Horizon instanatiation 
of VXLAN gateway at a nova-compute node.
We need to have nova-cloud-controller and vxlan-gateway deployed 
first and then put vxlan-gateway as a subornidate charm under 
nova-cloud-controller.

In the config.yaml you can provide general config that will
be common to all VXLAN Gateway in environement.

juju deploy [--config=<config file>]  nova-cloud-controller
juju deploy [--config=<config-file>]  vxlan-gateway
juju add-relation nova-cloud-controller vxlan-gateway

Contact Information
-------------------
Author: Dulanjalie Ganegedara ddhanapa@cisco.com

Report bugs at: http://bugs.launchpad.net/charms/+source/vxlan-gateway
Location: http://jujucharms.com/charms/distro/vem


