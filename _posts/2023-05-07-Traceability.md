---
title: Traceability
description: Traceability
excerpt: "This time I want to put a spotlight on the practice called traceability which  
is linked to another practice - reproducibility"
tags:
  - DevOps
  - Platform Engineering
  - Efficiency Engineering
---

This time I want to put a spotlight on the practice called traceability which  
is linked to another practice - reproducibility.  

In the worlds of CI/CD, the intention is to have a one-to-one value  
relationship between build artifacts and the version of the code from  
which the artifacts were built. That is, given a build artifact (container  
image, production environment, etc.) it is possible to track the code version  
without special effort.

(When I mentioned the term - build artifact in the previous paragraph, I meant  
its broad sense. It can include but not only - pypi libraries, operating  
system packages such as rpms, Terraform modules, Ansible playbooks and also  
container images.)

Simple on the face of it. Well... not really. Where do things get complicated?  
When our artifact consists of our code but also of artifacts of projects that  
are not ours (hereinafter - third party artifacts). For example:-  
the container image we produce is based on the parent image consumed from  
Dockerhub. And another example: - a production environment deployed on the  
basis of the IaC code that we develop with Terraform. But, we used the modules  
developed in other projects.

If so, we would like to include traceability not only on our code but also on  
third-party artifacts.  
Any self-respecting project releases versions. And given a version name, the  
code can be reached conveniently and without special effort.  
So, how does this relate to our project? Related for sure.  
When our project "consumes" the third party artifact it is documented in the  
code in one way or another. For example: when it comes to a container image,  
then write the parent image in the Dockerfile in the FROM instruction.

Continuing with the example. One option is to consume the latest version of  
the container image. A great option but one that breaks the traceability and  
hence also breaks the reproducibility. The latest tag is dynamic. Today points  
to one version, tomorrow to a newer version. Go try to restore your container  
image so that the result is the same as the image you made a week, a month, a  
year ago. I promise you it won't be easy.  
The second option is to use a tag that is fixed, the opposite of dynamic. And  
when a tag is like that, then it is convenient to get to the version of the  
code from which the container image was created with this tag.

And hence the phrase - to pin versions.

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
[2]: https://www.facebook.com/groups/devopsloft/posts/1835240793536116/
