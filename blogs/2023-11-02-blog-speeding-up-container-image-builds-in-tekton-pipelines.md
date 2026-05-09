---
title: "Blog: Speeding Up Container Image Builds in Tekton Pipelines"
url: "https://tekton.dev/blog/2023/11/02/speeding-up-container-image-builds-in-tekton-pipelines/"
date: "2023-11-02"
author: ""
feed_url: "https://tekton.dev/blog/index.xml"
---
Overview When DevOps or developer teams evaluate the move from a persistent CI server (or a CI server using persistent workers) to a system using non-persistent workers backed by Kubernetes pods, such as Tekton Pipelines, they might also wonder how to speed up container image building using cached layers. While using cached layers is relatively easy when builds always run on the same server where layers can be stored locally, it is more challenging in an environment where the builds are run in non-persistent containers on Kubernetes.
