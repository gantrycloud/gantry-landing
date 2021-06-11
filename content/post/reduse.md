---
title: "RED+ vs USE Method"
date: 2020-05-12T12:14:34+06:00
image: "images/reduse.jpg"
author: "Jason Stryker"
description: "RED+ VS USE Methodology"
categories: ["DevOps"]
tags: ["Services"]
draft: false
---


# The Red Use methodology

The use of USE vs RED metrics as they apply to infrastructure resources is a powerful paradigm allowing for more efficient and reliable applications. Starting by isolating workload metrics from hardware metrics, one can improve performance from both ends.

USE metrics are used to understand how applications behave and where they should be scaled. This metric correlates with load, memory usage, CPU useage, etc. so it is great for understanding what the application needs in order to function properly. In contrast RED metrics compare infrastructure resources against each other using a scale that ranges from 0% utilized (green) -> 100% utilization (red). Monitoring and Observability With USE and RED on Kubernetes

It’s worth noting that both sets of metrics have an important role: by isolating workload metrics such as CPU or Memory we can see if there are any spikes which would indicate issues coming up; meanwhile monitoring red metric thresholds allows us to know when scaling out/in.

A great article diving further into the fundamentals of USE/RED can be found at https://orangematter.solarwinds.com/2017/10/05/monitoring-and-observability-with-use-and-red/

Applying it to kubernetes is a separate matter. Some prometheus metrics to look for RED metrics are

- load_one

- node_load (if you have num nodes)

- memory usage on the node.

- cpu utilization of a pod and other pods it is cohabiting with in terms of resource requirements as well as aggregate metrics such as user, system or wait time. Monitoring these would allow us to identify issues proactively rather than relying solely on alerts which can be noisy! This also provides visibility into what resources are being used by any given workload. Once we know that threshold has been reached, scaling out if necessary would help prevent cascading failures due to higher latency for requests since there will no longer be enough capacity where service levels are not met anymore. Scaling up when thresholds have been cleared allows new nodes.



Some USE metrics to pull from prometheus are:

- CPU, memory and network utilization by pod.

- Memory and disk usage of a node (incl the aggregate over all pods on that node).

- Number of requests per second for particular services or nodes.

- Latency for various operations with some more specific USE metrics available in prometheus when we set up our own toolsets to collect data from multiple sources.

Some RED metrics:

Memory is not something you can reserve but it becomes important if other resources are scarce as it determines how much work your application will be able to do at any given time so this metric would also come in handy during times where scaling out might not help anymore due to higher latency. When using containers, there's always an overhead



Because the human observer can better perceive things visually, we need to display these somewhere. The best way to then monitor these will be with Grafana, an open source graphing tool geared towards kubernetes. Metrics can change color based on the health of the metric.





Monitoring and observability with USE and RED on Kubernetes

The human observer can better perceive things visually, so we use Grafana as a graphing tool to monitor our metrics. Metrics change color based on the health of the metric. Some red metrics are memory which is not reserved but becomes important if other resources become scarce, or latency that's higher when scaling out might no longer help due to scarcity in CPU. Setting up your own toolsets can be useful too for more data points than what you get from default monitoring solutions like Prometheus. Monitoring/Observability With USE And RED On Kubernetes Learn how an organization was able to set up their own toolsets (such as Telegraf) to



Wrapping up, it is important to instrument your services properly based on the type of service and the expected number of requests. To be clear, this is not a fix for shoddy code but it can help greatly if an application has an overuse of concurrency to make up for lack of performance.





It is also important to be able to monitor how your application behaves in production. For this, you will want some form of observability such as USE and RED on Kubernetes. Learn how an organization was able to set up their own toolsets (such as Telegraf) together with techniques like service discovery and understanding load balancing patterns



Wrapping up, it is important if other resources become scarce or latency that's higher when scaling out might no longer help due to scarcity in CPU - for example, setting the number of pods per node can only go so high before there are too many containers contending for the same resource; even though more CPUs would make better use of available memory. Setting up your own toolsets
