dockerpress
===========

A Dockerfile to build self-contained preconfigured Wordpress installations

Requirements
=============

To make the system completely automated, install the following containers first:

1. NS-ENTER 

	docker run --rm -v /usr/local/bin:/target jpetazzo/nsenter

2. NGINX-PROXY

	docker run -d --name hostmanager -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock jwilder/nginx-proxy


Building the Image
==================

To build the image, run this commmand:

	docker build -t "dockerpress" .


Running the Image
=================

	docker run  -d -P -t dockerpress


