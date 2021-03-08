---
title: "UniHelm"
date: 2018-05-12T12:14:34+06:00
image: "images/helm.png"
author: "Mark Wagner" # use capitalize
description: "Unified Helm Kustomize"
categories: ["consulting"]
tags: ["Dev-Ops"]
draft: false
---
Unifying your helm.. is it a good idea?

So you have twenty microservices floating around with their own values files, stateful sets, service yamls and possibly even pulling from isolated sources of secrets. 

This can be hard to maintain, depending on your CI pipeline due to the fact that each values file needs to have its versions modified every time a new container is made, tagged and pushed to the repository. 

In one instance, we had a gitlab ci pipeline runner that would run the docker build and put the container in google cloud repository upon tagging. Then when deploying the helm charts, each chart would self-reference in the _helpers.tpl, NOTES.txt, and stateful sets/deployment/service yamls. This was a source of some frustration attributable to the following:
- Too many files
- Pipeline updates cannot be version controlled on one values yaml
- Observability on Declarative platforms (such as argo)

Initially, our ARGO dash appeared as if there were many unrelated applications running:

<See Image>

After combining the helm charts into one, with a handy script I wrote, our ARGO setup appeared beautifully as this:

<See Image>

Now, not only do we have the option of rolling back using the kubernetes controller, but we could roll back the values yaml itself to prior versions. 

We instead set up the gitlab runner to go into the unified-helm chart repository and update the values yaml each time a release was tagged in the source repos by any of our engineers.

So the lesson is: Unless otherwise required, wield helm in a manner that is most powerful for your team and your infrastructure. 

Mark
