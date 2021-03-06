---
title: "Argo CD"
date: 2018-05-12T12:14:34+06:00
image: "images/argo.png"
author: "Jason Stryker" # use capitalize
description: "This is meta description."
categories: ["main"]
tags: ["Systems"]
draft: false
---

# Why not declarative?

Have you ever written a deploy script to push your Kubernetes Helm chart yamls up to the cluster one by one?

Maybe you do this manually and then have the misfortune of having to do it all over once more when something breaks.

ArgoCD is a powerful tool that runs in your cluster and grabs everything it needs from github/gitlab including:

* Container Repository Locations
* Helm Charts
* Latest Tags

It then executes the helm command as a "sync" in your cluster and puts it all together in a beautiful visual graph.

In addition, all your work is saved and can be rolled back to with the click of a button.

ArgoCD is the first and last thing you should be installing on your cluster if you are running helm charts with a dynamic team workflow.

Ask us how you can rapidly make this your CD setup!
