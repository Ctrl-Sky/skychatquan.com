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

# A Quick Look at the Project
This project automatically spins up an AWS EC2 instance with a configured VPC, a firewall with open HTTP, HTTPS, and SSH ports

# Tools Used
* Linux
* Cloudflare
* AWS EC2
* Terraform
* Ansible
* Github Actions
* Markdown

# The Purpose for Creation
The main reason I created this website is because I wanted to learn more about Terraform and Ansible. Having completed my year long DevOps Engineer Internship just a couple of months ago, I found I was still lacking a lot information in the infrastructure department. Having worked closely with the infrastructure team, I heard a lot about Terraform and the "cloud" but never really got the chance to work with it personally. So, I finally took it upon myself to learn about infrastructure and the automation behind it. I came up with the idea to create a static site because it fit my requirements perfectly, firstly, I get to learn Terraform and Ansible through the process of spinning up and configuring the server and secondly, I finally get an excuse to get a domain and create a unified place to show off my experience and projects.