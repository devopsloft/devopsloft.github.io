---
title: Paved Paths 2
description: Paved Paths
excerpt: ""
tags:
  - DevOps
  - Platform Engineering
  - Efficiency Engineering
  - Engineering Enablement
---

Following on from last week's post. The series of blog posts talks about paved
paths.  
I won't tell you what it means. Read the series (which is not yet completed).
The writers explain it really well and clearly.  
I have been thinking with myself since I came across the topic about how it is  
actually applied in the environment I work in.  
It's true, it's still WIP (work in progress). But, I already have several  
processes and technologies that I can put on the table here.  
Below is my initial list:-

* Static code analysis - [pre-commit][3]. I make sure every project I work on
  including open source projects, are onboarded.  
  There are several areas in the development lifecycle it can be applied:
  * Locally, by IDE extensions which warn/correct while editing the code
  * Locally, which is triggered by the `git commit` command
  * In CI, catching the cases where it was not run locally
* Automatic dependency update - [renovate][4]. I've been digging into this topic
  quite a bit in the last few weeks. Say no more.
* A development environment inside a container. Instead of installing and
  maintaining on my computer(s) all the tools required to run an environment
  all that is required is docker or podman or any other containers engine.  
  Two options for activation:
  * Local - [devcontainer][5]
  * Remote - [codespaces][6] or [gitpod][7]

I have dug enough and therefore I will go to the stage of the identical
questions:-  
Did this post bring you new insights?  
Did you learn something you didn't know before?  
Have you faced a similar challenge in a different way? in different tools?  
A good and magical week.

P.S. Want to talk to me one on one. Click on
[link][1].

Original Facebook post in Hebrew [here][2]

[1]: https://calendly.com/lmilbaum/chitchat
[2]: https://www.facebook.com/groups/devopsloft/posts/1843968359330026/
[3]: https://github.com/pre-commit/pre-commit
[4]: https://github.com/renovatebot/renovate
[5]: https://github.com/devcontainers
[6]: https://github.com/features/codespaces
[7]: https://www.gitpod.io/
