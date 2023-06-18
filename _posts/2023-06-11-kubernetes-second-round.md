---
title: Kubernetes - second round
description: Kubernetes - second round
excerpt: "Summary of the previous chapters on the way to the destination -
kubernetes"
tags:
  - DevOps
  - Platform Engineering
  - Efficiency Engineering
  - Engineering Enablement
---
Summary of the previous chapters on the way to the destination -
[kubernetes][3]:  
I started with the project itself but encountered difficulties due to the
architecture of my laptop- macOS M1. I tried [kind][4] which worked quite nicely
and also [colima][5]. Both worked on the laptop but I was not able (in the short
time I invested in them) to use them in CI. And finally, I got to [minikube][6]
thanks to one recommendation from last week. I have an environment that works
both locally (development environment) and there is also an environment that
works in CI. And when I say local I mean the [dev container][7] environment.
This was made possible because there is a [feature][8] that fit me like a charm.
Oh, one more little detail… I proceeded to install gitlab ci runner using
[helm chart][9] and it worked like a dream.  

What's more, I haven't yet found the elegant way to share secrets in both
environments. Right now, I'm using the values file in the DEV environment.
While in the CI environment I use [GitHub Secrets][10]. Not the [DRY][11]est to
say the least. A tech debt that I will close as soon as possible.  

And below is the [project][12] in which I implemented the entire tech stack
mentioned above.  

I have dug enough and therefore I will go to the stage of the identical
questions:-  
Did this post bring you new insights?  
Did you learn something you didn't know before?  
Have you faced a similar challenge in a different way? in different tools?  

P.S. Want to talk to me one on one. Click on
[link][1].

Original Facebook post in Hebrew [here][2]

[1]: https://calendly.com/lmilbaum/chitchat
[2]: https://www.facebook.com/groups/devopsloft/posts/1857065694686959/
[3]: https://github.com/kubernetes/kubernetes
[4]: https://kind.sigs.k8s.io/
[5]: https://github.com/abiosoft/colima
[6]: https://minikube.sigs.k8s.io/docs/
[7]: https://containers.dev/
[8]: https://github.com/devcontainers/features/tree/main/src/kubectl-helm-minikube
[9]: https://docs.gitlab.com/runner/install/kubernetes.html
[10]: https://docs.github.com/en/actions/security-guides/encrypted-secrets
[11]: https://en.wikipedia.org/wiki/Don%27t_repeat_yourself
[12]: https://github.com/platform-engineering-org/gitlab-ci-runners
