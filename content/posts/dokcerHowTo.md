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
Normally a project comprises configuration plus code, such project requires compilation per environment, to package correct configuration.
Usually when moving towards Containerization, it a good practise to remove configuration from code, by following such practise the code needs to be compiled only once.
While the environment specific values injection happens at runtime.

This way we make sure the image used to create containers, and the code is same across all the environments.

By doing so we have made two things static 
* runtime code
* runtime environment

Now if the code works on your machine and on Development environment but fails on Test Environment, we can narrow it down to either configuration or database issue.

### Docker Website and Installation

Since we have decided to use docker for containerization, let us now visit the Docker website (https://www.docker.com/).
Click on getting started with Docker and follow the installation steps as explained on the website.

If you want to quickly try Docker without installing it first, you can visit Play with Docker website, which will give you a Linux environment to run Docker commands.

### Checking Docker version

If you did the docker installation then to check if the installation was successful.

* For Linux or OSX, open your favourite terminal.
* Open Git Bash or Terminal Emulator of your choice on windows, if you do not have any terminal emulator then, oh well command-prompt it is.

Next run command: docker version

You should see both client and server version.

* If on linux you get the below error, where Docker is unable to pull server details :

![docker version](/images/docker_as_user.png)

* Then re-run the command using sudo:

![sudo docker version](/images/docker_using_sudo.png)

If on windows you see any errors, well in that case Google is your friend.

### Checking Docker Images on DockerHub

* https://hub.docker.com/

Here the main thing to look for is the difference between official and un-official images.

Snippet from 'https://docs.docker.com/docker-hub/official_images/'

New Docker users are encouraged to use the Official Images in their projects. 
These images have clear documentation, promote best practices, and are designed for the most common use cases. 
Advanced users are encouraged to review the Official Images as part of their Dockerfile learning process.

A common rationale for diverging from Official Images is to optimize for image size. 
For instance, many of the programming language stack images contain a complete build toolchain 
to support installation of modules that depend on optimized code. 
An advanced user could build a custom image with just the necessary pre-compiled libraries to save space.

All official images repositories will have te label 'Docker Official Images' on them.

Each of the images in the Official Images is scanned for vulnerabilities. 
The results of these security scans provide valuable information about which images contain security vulnerabilities,
and allow you to choose images that align with your security standards.

### Checking Docker Images On Local

On your favourite terminal please run command: 

docker images

if you get permission denied error then please try running using sudo:

sudo docker images

### Pulling Nginx Image From DockerHub

* Please goto www.dockerhub.com
* On the search bar type "nginx"
* Select the repository labelled "Docker Official Images" and "Official build of Nginx"
* Clicks on Tags to see what all different versions on Nginx images are available
* Select a tab, example 'latest'
* Then on your machine, open your favourite terminal and type 'docker pull nginx:<Tag>' example: docker pull nginx:latest
* if you simply run 'docker pull nginx' then it will pull 'latest' tag by default.

### Checking running containers

To see all running containers please run the below command:

'docker container list' or 'sudo docker container list' depending on your docker process requirement 

### Assignment
* Checkout Docker.com
* Checkout DockerHub.com
* Try finding some official repos of your favourite software.
* Try pulling amd running a few images from DockerHub locally
* Check what all images you have pulled locally
* Check what containers are running locally
* Specify a container name when starting the container
* Start a container and get Shell access to that container, as soon as it is started by using a single command
* Stop a running container
* Start a stopped container 
* Get Shell access to the started container
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