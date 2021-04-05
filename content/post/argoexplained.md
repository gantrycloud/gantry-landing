---
title: "Argo Explained"
date: 2021-04-05T15:19:28-07:00
image: "images/argocd-ui.gif"
author: "Mark Wagner" # use capitalize
description: "argocd continuous delivery kubernetes CICD"
categories: ["main"]
tags: ["Services"]
draft: false
---

1. Argo is a free, open-source continuous deployment tool
2. It's designed to be easy to use and deploy with any language or framework
3. It works by running commands on your servers as you push new code to GitHub
4. You can configure it for automatic deployments using web hooks from GitHub or BitBucket
5. When deploying, Argo will run tests before updating the server if necessary
6. If tests fail, then no changes are made and the previous version of the app remains deployed until you manually update it yourself (or fix the tests)
7. Argo also has an option for staging environments that let you test out new features before they go live in production
