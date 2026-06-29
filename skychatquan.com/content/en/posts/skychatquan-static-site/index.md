---
title: skychatquan.com Static Site
date: 2026-06-16
author: Sky Quan
description: Description of skychatquan.com static site project
tags:
  - project
---

This post details my work on this VERY website and how its creation came to be. The code can be found on my github here: 
* The Infrastructure: https://github.com/Ctrl-Sky/skychatquan-infra.git
* The Website: https://github.com/Ctrl-Sky/skychatquan.com.git 

# Project Overview
This project uses Terraform and Ansible to automatically spin up and configure an AWS EC2 instance for hosting my personal website. This website is created via Hugo and automatically deployed to the server with each push to the website repo. Additionally, Nginx is used as the webserver to handle HTTP request and Cloudflare is used as the DNS provider.

To get into the specifics, on the infrastructure side, this project uses Terraform, hooked up to AWS and Cloudflare, to automatically spins up an AWS EC2 instance and configure a VPC, a firewall with open HTTP, HTTPS, and SSH ports, a static IP for the server, and attaching that static IP to Cloudflare for DNS. After the EC2 instance is spun up, the static IP is passed to Ansible where it SSHs onto the server and begins to configure it. There, Ansible creates users for Github Actions deployment, installs and configures nginx to correctly handle HTTP request, and uses Let's Encrypt Certbot to receive an SSL certificate. 

On the website side, the website content is written onto markdown and Hugo is used to convert the markdown into HTML, CSS and JS. The changes are taken by Github Actions and automatically built and deployed to the server.

# Tools Used
* Linux
* Nginx
* Cloudflare
* AWS EC2
* Terraform
* Ansible
* Github Actions
* Markdown

# The Purpose for Creation
The main reason I created this website is because I wanted to learn more about Terraform and Ansible. Having completed my year long DevOps Engineer Internship just a couple of months ago, I found I was still lacking a lot information in the infrastructure department. Having worked closely with the infrastructure team, I heard a lot about Terraform and the "cloud" but never really got the chance to work with it personally. So, I finally took it upon myself to learn about infrastructure and the automation behind it. I came up with the idea to create a static site because it fit my requirements perfectly, firstly, I get to learn Terraform and Ansible through the process of spinning up and configuring the server and secondly, I finally get an excuse to get a domain and create a unified place to show off my experience and projects.