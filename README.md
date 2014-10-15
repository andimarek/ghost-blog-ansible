# Ansible based setup of a Ghost blog 

This is an example how to setup a [Ghost](https://ghost.org) blog with [Ansible](http://ansible.com). 

It includes:

 - Haproxy and Ghost running as Docker containers
 - [nsenter](https://github.com/jpetazzo/nsenter) to inspect a running container
 - SSL Support

The ansible ssh user to connect the server must be root.

It was successfully tested with Ubuntu 14.04 but it is not working out of the box, 
because you need to modify your server and blog specific settings:
 
 - Ansible `hosts` file
 - Ghost config `roles/ghost/files/config.js` and themes `roles/ghost/files/themes`
 - Add your own SSL certificate: `roles/haproxy/files/example.com.pem` 
 - Modify the haproxy config: `roles/haproxy/files/haproxy.cfg`


Helpful resources:
 - [SSL Termination with haproxy](https://www.digitalocean.com/community/tutorials/how-to-implement-ssl-termination-with-haproxy-on-ubuntu-14-04)
 - [Docker and IPv6](http://gesellix.net/docker-and-ipv6-on-ubuntu-13-10-saucy-salamander/)
 - [Ansible Docker role](https://github.com/angstwad/docker.ubuntu)

I hope somebody finds this useful. 

If you have any questions or comments: One way to get in touch with me is via Twitter [@andimarek](https://twitter.com/andimarek)

