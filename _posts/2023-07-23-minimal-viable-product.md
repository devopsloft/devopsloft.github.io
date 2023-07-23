---
title: Minimal Viable Product
description: Minimal Viable Product
excerpt: "Last week I shared that I started working on a slightly different
project than usual. Managing the permissions scheme for the tree of Git projects managed in the namespaces tree in Gitlab."
tags:
  - DevOps
  - Platform Engineering
  - Efficiency Engineering
  - Engineering Enablement
---
Last week I shared that I started working on a slightly different project than
usual. Managing the permissions scheme for the tree of Git projects managed in
the namespaces tree in Gitlab.  
As [Evgeny][2] pointed out in the comments, one of the tools that might be
suitable is [backstage][3]. There are of course other tools in this domain.
[port][4] is one of them.  
Strategically, this is definitely the right direction to go with, but on a
tactical level, when the chaos reigns and the engineering work is stuck due
to imprecise permissions, it is important to provide a tactical response. I call
it - MVP or alternatively quick and dirty solution.  
For the benefit of my project, I chose [terraform][5] as a development tool to
help me code the configuration. In addition, I decided (and not for the first
time) to break the deployment into very small parts. And each time deploy a
small change, stop, check the pulse and only after making sure that everything
is good to move on to the next step.

I have dug enough and therefore I will go to the stage of the identical
questions:-  
Did this post bring you new insights?  
Did you learn something you didn't know before?  
Have you faced a similar challenge in a different way? in different tools?

Original Facebook post in Hebrew [here][1]

[1]: https://www.facebook.com/groups/devopsloft/posts/1882742192119309/
[2]: https://www.facebook.com/ybgny.pynqyn
[3]: https://backstage.io/
[4]: https://www.getport.io/
[5]: https://www.terraform.io/
