---
title: Kubernetes - Gitlab runner
description: Kubernetes - Gitlab runner
excerpt: "I'm still on a journey to acquire kubernetes knowledge. The tech
wealth (with light sarcasm) is significant."
tags:
  - DevOps
  - Platform Engineering
  - Efficiency Engineering
  - Engineering Enablement
---
I'm still on a journey to acquire [kubernetes][3] knowledge. The tech wealth
(with light sarcasm) is significant.  
I made a little progress last week. In the previous chapter I shared that I
encountered a problem sharing secrets in both environments: DEV & CI. So, I just
wanted to say that I got good feedback from you and others and in the end I
chose to go with [kustomize][4]. I came across this technology years ago but
only now the insight, why it is good, landed. What's more, it seems to me that
the kubernetes community has officially adopted this technology (which probably
wasn't the case when I first encountered it).  

A short summary of what is already working in the [project][5]:

* DEV environment using [devcontainer][6] and the [feature][7]

* Uploading and downloading the environment using [make][8], [minikube][9],
  [kustomize][4] & [helm][10]

* CI environment using [GitHub Actions][11] & [GitHub Secrets][12]

What's more, I encountered a problem that started as soon as I transferred the
Gitlab Runner Token from the values file to the secret stored in the cluster.
When I download the environment, the registration of the runner is not deleted.
I made quite an effort to locate the problem and even tried to fix it. But I
still haven't found a solution. And when I reach a kind of dead end, I [turn to
the general public][13], which is the community. There are two options. Either I
have a problem with the configuration or it's a bug. I believe that I will have
a proper answer by the next chapter.  

I have dug enough and therefore I will go to the stage of the identical
questions:-  
Did this post bring you new insights?  
Did you learn something you didn't know before?  
Have you faced a similar challenge in a different way? in different tools?  

P.S. Want to talk to me one on one. Click on
[link][1].

Original Facebook post in Hebrew [here][2]

[1]: https://calendly.com/lmilbaum/chitchat
[2]: https://www.facebook.com/groups/devopsloft/posts/1861548744238654/
[3]: https://github.com/kubernetes/kubernetes
[4]: https://github.com/kubernetes-sigs/kustomize
[5]: https://github.com/platform-engineering-org/gitlab-runners
[6]: https://containers.dev/
[7]: https://github.com/devcontainers/features/tree/main/src/kubectl-helm-minikube
[8]: https://www.gnu.org/software/make/
[9]: https://minikube.sigs.k8s.io/docs/
[10]: https://github.com/helm/helm
[11]: https://github.com/features/actions
[12]: https://docs.github.com/en/actions/security-guides/encrypted-secrets
[13]: https://forum.gitlab.com/t/gitlab-runner-helm-chart-runner-is-not-unregistering-when-using-secret/88389
