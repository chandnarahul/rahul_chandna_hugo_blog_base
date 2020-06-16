---
title: "Docker Self Help"
date: 2020-06-16T12:13:12+02:00
description: This article gives an introduction to Docker.
tags: Docker
categories: "Containerization"
---

### Journey From Mainframe To Docker

Initially all corporations used Mainframes but what everyone quickly realised is that most of the time hardware sat idle.
 
This raised a demand to find ways to better utilise the hardware in such a way that compute is not only shared for multiple tasks 
but also provides guaranteed process isolation and security.

To solve this companies like VMware created software which is installed directly on bare-metal, 
we can then on top of this software depending on how powerful the bare-metal is install any number of supported operating systems such as windows or linux. 

So far all of this is for sysadmins, people who are interested in or understand the core software virtualization concepts, because only they have access to configure operating systems and resources as required bby a team.

As you can guess this does not include or take into consideration the software developer, these things in most organisations come into play when the software is ready to be deployed, in some cases it is used to provide a virtual development environment but again the developer is more of a "user".

This brings us to containerization.

Containers (serverless, function-as-service) is basically the next shift in the way the entire application, or a single piece of functionality runtime is configured.
It provides an isolated way to run application from rest of the system, this makes it a lightweight process running an application on existing Operating System.

* rkt from CoreOS
* Mesos by Apache
* containerd
* LXC

#### For Entire List and details, please visit:
* https://www.ionos.com/digitalguide/server/know-how/docker-alternatives-at-a-glance/

Docker workflow includes developer, this means it can be used by Dev's as well as sysadmins.

At this point obviously we will be running containers manually, and will be skipping on demand or under heavy load container provisioning, networking, load-balancing, security and scaling. 

### Why build once and deploy multiple times


### Docker Website and Installation


### Checking Docker version


### Checking Docker Images On Local


### Checking Docker Images on DockerHub


### Pulling Nginx Image From DockerHub


### Checking running containers


### Assignment
* Checkout Docker.com
* Checkout DockerHub.com
* Checkout Cloud Native Computing Foundation landscape.cncf.io

### Understanding difference between Docker Image and Container


### Running Nginx Image


### Logging on to Nginx container via shell


### Port Forwarding Nginx image internal port 80 to Laptop Port 8080


### Accessing Nginx on Laptop via Browser by going to http://localhost:8080


### Assignment


### Stopping Nginx Container


### Starting Nginx Container


### Introduction to Dockerfile


### Reducing the amount of re-work by creating a Dockerfile to do above steps for us


### Understanding Java structure and how to add custom Certificates to keystore


### Assignment


### Understanding WildFly server


### Checking DockerHub for Java +WildFly image


### Compiling a Java EE Application that produces WAR file


### Running Docker WildFly Image manually


### Port forwarding Wildfly container 8080 to Laptop 8080


### Accessing docker container Wildfly instance from Laptop Browser by going to http://localhost:8080


### Copying war file manually into running WildFly Docker container


### Accessing the deployed war running in Docker WildFly container from Laptop Browser by going to http://localhost:8080


### Assignment


### Adding Dockerfile to our web application project


### Adding all manual commands to Dockerfile


### Running Dockerfile


### Testing Dockerfile execution worked properly by accessing the application from Laptop Browser by going to http://localhost:8080