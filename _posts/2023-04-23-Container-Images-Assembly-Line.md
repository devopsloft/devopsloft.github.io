---
title: Container Images Assembly Line
description: Container Images Assembly Line
tags:
- DevOps
- Platform Engineering
- Open Source
- Renovate
- Containers
- Docker
- CI/CD
---
Original Facebook post in Hebrew [here][0]

Good morning and good week,

This week I took a break from the serial story and focused on something a  
little different.  

Building a family of container images. That is, we have a container image  
which is the parent of container images. I mean, we already have two  
generations in the family. There are container images in the second generation  
that are themselves ancestors of container images. This is how a third  
generation was created. and so on and so on. You never know where it will  
stop.
When a new version of the parent container image lands, you have to rebuild  
its son. And when a new version of the son lands, then the grandson also needs  
to be built. etc. etc. etc. You get the idea. Right?

Oh, and one more thing. Each container image has additional dependencies and  
sometimes you have to rebuild a son or grandson regardless of whether the  
father has changed or not. In short, there is complexity here.

So much for the background story.  
The challenge is how to optimize the process so that the construction process  
is:

- Automatic. It doesn't make sense for a human to orchestrate the process.

- Effective. We will build only what needs to be built and we will not build  
  if there is no reason for it.

- The quality of the artifacts is not affected. How do you test each new build  
  like this without troubling the QA team.

- Maintainable. The process can be debugged if something has gone wrong.

Below are the main points of the solution based on an open source project that  
I got excited about not long ago - [Renovate][1].  
Basically, the tool is designed for dependency update automation. This is  
exactly what is required here assuming that he knows how to identify these  
dependencies. And I'll tell you a known secret - it knows how to detect  
dependencies between container images. Yay.  

So now all that remains is to make a small poc.  
I chose the git repo of a son container image. And in this repo there is a  
Dockerfile with a reference to the parent container image. And the father is  
ours. That is, the container image that our factory produces.  
Our container images land in self-hosted container registries or private image  
repositories.  
All that's left to do is:

1. Make sure that the tag of the parent image is pinned and not some floating
   tag, heaven forbid  

1. Configure self-hosted renovate  

1. Make sure that renovate has access to the container image repositories (it  
   seems a simple step. Not necessarily. For me it took days until it started  
   working)  

1. Make sure that Renovate knows how to process your tag schema (assuming it's  
   not standard)  

Let's party. The poc is ready for demo.  
Those who want to see it should say: me!!!  

In conclusion, I'll just say and add that the why is one that I've been  
thinking about for quite some time. Each time I found a tool that I thought  
was it and that I could run with. And in the end, it wasn't that. And now, I  
think I've reached a state of tranquility.  

I have dug enough, so I will move on to the identical questions stage:-  
Did this post bring you new insights?  
Did you learn something you didn't know before?  
Have you faced a similar challenge in a different way? with different tools?  

Have a good and magical week.  

P.S. Want to talk to me one on one. With pleasure. Click on the [link][3].

[0]: https://www.facebook.com/groups/devopsloft/posts/1826609207732608/
[1]: https://docs.renovatebot.com/
[3]: https://calendly.com/lmilbaum/chitchat
