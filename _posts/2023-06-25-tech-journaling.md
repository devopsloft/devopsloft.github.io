---
title: Tech Journaling
description: Tech Journaling
excerpt: "Lately I've had an aha moment that this group has become my personal
travel diary into the ins and outs of DevOps and Platform Engineering"
tags:
  - DevOps
  - Platform Engineering
  - Efficiency Engineering
  - Engineering Enablement
---
Lately I've had an aha moment that this group has become my personal travel
diary into the ins and outs of DevOps and Platform Engineering.
I came to know that I learn a lot through the journeys of others and also from
my own journey. A significant part of my time is devoted to exchanging opinions
with people from the industry, colleagues and even with those who work at Red
Hat but not in my organization. I highly recommend the practice.
I hope that one day this group will serve not only me. There is something
empowering about unpacking and receiving feedback.

Just FYI, I'm still on a quest to acquire [kubernetes][3] knowledge. The journey
is going to be long and tiring. I realized that I have many holes in my
education. Remember the problem I ran into in the previous chapter? (Do not
answer, rhetorical question). I recalculated my route and realized that I was
trying to mix a DEV environment with a PROD environment, so the problem is a
problem. The runner that remains "registered" in the PROD environment pollutes
my environment. The conclusion is that there is no way to mix the environments.
I need a gitlab server in the DEV environment. One that is created when I deploy
an environment and one that is torn down when I don't need it.
And therefore, I switched to a [helm chart][4] that knows how to deploy both the
server and the runner in one operation. It turns out there is one. Maybe in the
future I will split, but right now it seems like a more correct move.  
This move also creates new challenges that I still can't solve. It turns out
that the domain parameter is a mandatory one. The domain is used to access the
console or whatever you call it. Well… to the GitLab UI. But, I don't have local
dns when I deploy [minikube][5] inside [devcontainer][6]. And to complicate
matters, browsing is done in a browser running on the host while the server runs
in a container running on the host. The plot gets complicated. There is a
situation where I put myself in hopeless challenges.
Of course I did the obvious and addressed the [general public][7] for help. This
time to the community of Gitlab users on Discord. Maybe salvation will come from
there. Until then I populated the parameter with something completely
[random][8].

I have dug enough and therefore I will go to the stage of the identical
questions:-  
Did this post bring you new insights?  
Did you learn something you didn't know before?  
Have you faced a similar challenge in a different way? in different tools?  

P.S. Want to talk to me one on one. Click on
[link][1].

Original Facebook post in Hebrew [here][2]

[1]: https://calendly.com/lmilbaum/chitchat
[2]: https://www.facebook.com/groups/devopsloft/posts/1865598790500316/
[3]: https://github.com/kubernetes/kubernetes
[4]: https://gitlab.com/gitlab-org/charts/gitlab
[5]: https://minikube.sigs.k8s.io/
[6]: https://containers.dev/
[7]: https://discord.com/channels/778180511088640070/1122227859201740820/1122227859201740820
[8]: https://github.com/platform-engineering-org/gitlab-runners/blob/main/values.yaml
