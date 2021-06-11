---
title: "Kustomize"
date: 2019-03-05T20:45:43-07:00
image: "images/kustomize.png"
author: "Mark Wagner" # use capitalize
description: "This is meta description."
categories: ["consulting"]
tags: ["Open Source"]
draft: false
---

## How do Kustomize and Helm Compare?  
&nbsp;

Helm and Kustomize are two tools that allow users to create custom Linux-based OS stacks for cloud environments. The only difference between these two is in how they work with Docker containers. Kustomize builds on top of a base image, whereas Helm creates a new container instance from scratch. Kustomize does not have built-in support for using Docker images as templates, but has an ability to use any other tool such as Ansible or Chef. Helm also doesn't have built-in support for using Docker images as templates, but it can be extended via plugins or scripts if desired. 

Helm is an open-source project that was started by Google and has quickly grown in popularity due to its ease of installation and configuration. The goal of the project is "to make building repeatable, reliable, and portable systems easier." In this blog post I'll show you how easy it can be to deploy applications with just a few commands!  

Kustomize is a tool for templating application deployment, which enables users to customize the way their applications are deployed. It does this by providing an interface that allows you to specify what commands and options should be executed during installation. This blog post will show you how to use Kustomize in order to template your deployment process so that it's tailored specifically for your needs.  

In other words, Kustomize is more of a tool for managing images while Helm offers something akin to templates. However there are many similarities as well such that both offer the ability configure and provision containers with configuration information defined in files rather than code or command line parameters which makes them very suitable choices when dealing specific tasks like deploying an application stack at scale using multiple instances (e.g. microservices) because they allow you do this without having deep knowledge about the Dockerfiles nor getting into the weeds with Kubernetes - all tools are provided with preconfigured option sets from their respective repositories based on your needs/requirements specified in the config yaml.

 We'll discuss what you need in order to build and deploy containers with Kustomize on Kubernetes!
 Lets go over a few steps that are needed for this process:

```
 - First, create a new Kustomize file in your directory of choice.
   The name can be anything you would like, but it should end with the .kts extension to make sure that kdevelop knows how this is set up as an application template for deployment purposes.  

 - Open Terminal and cd into where we just created our newly named folder (in my case I'm using ~/projects). Type 'ksubmake -t appname' This will create all files needed by other commands used when setting out on installing apps via terminal or SSH connection...etc.. If any errors occur at anytime during installation please consult documentation listed below such +http://devdocsxpressblog/articles/. After running command enter ls again.  

 - Create an account at Docker Hub so our applications can be built by using their official images  

 - Clone kubercustomizer/kubectl which contains all of its source code repository files into ~/git_code/  

 - Navigate back inside terminal cd ~\git\code and type python setup . py develop - p ./src/configs  

 - Finally install jinja because it will serve to...

 Continue Reading on our tutorial posts.  
```
