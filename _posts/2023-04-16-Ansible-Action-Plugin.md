---
title: Ansible Action Plugin
description: Ansible Action Plugin for k8s connection
excerpt: "Returning to the ongoing, never ending story. At issue is an Openshift cluster  
running on AWS on which Gitlab CI Runner will be installed. And all this  
goodness through automation."
tags:
- DevOps
- Platform Engineering
- Ansible
- k8s
- AWS
- Open Source
- Gitlab CI
- GitHub
---
Original Facebook post in Hebrew [here][0]

Returning to the ongoing, never ending story. At issue is an Openshift cluster  
running on AWS on which Gitlab CI Runner will be installed. And all this  
goodness through automation.  
For now, I chose Ansible to be the automation wrapper. I don't know if it's  
the best choice, but it's good enough for MVP. In the future there is a  
situation where I will improve positions.  
For the benefit of the future CI I found a [project][1] that spins a cluster  
on AWS with a small footprint. One that consumes relatively few resources and  
also spins relatively quickly. Something like 15 minutes.  
At this time I face a tiny challenge. Ansible has a nice feature.
Action Plugin.  
I thought it appropriate to utilize it for the benefit of all the tasks in  
the playbook that configure the cluster.  
The idea is to use it for the connection. My tasks would look cleaner.  
Minimal repetitive code.  
Well... this practice that says - don't repeat yourself.

This part is still a work in progress. Anyone familiar enough with Ansible to  
help me?

I have dug enough and therefore I will go to the stage of the identical
questions:-  
Did this post bring you new insights?  
Did you learn something you didn't know before?  
Have you faced a similar challenge in a different way? in different tools?  
A good and magical week.  

P.S. Want to talk to me one on one. Click on [link][3].  

[0]: https://www.facebook.com/groups/devopsloft/posts/1822520201474842/
[1]: https://github.com/crc-org/crc-cloud
[3]: https://calendly.com/lmilbaum/chitchat
