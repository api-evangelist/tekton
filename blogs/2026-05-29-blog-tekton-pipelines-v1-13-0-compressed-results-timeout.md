---
title: "Blog: Tekton Pipelines v1.13.0: Compressed Results, Timeout Fixes, and Observability"
url: "https://tekton.dev/blog/2026/05/29/tekton-pipelines-v1.13.0-compressed-results-timeout-fixes-and-observability/"
date: "2026-05-29"
feed_url: "https://tekton.dev/blog/index.xml"
---
We’re excited to announce the release of Tekton Pipelines v1.13.0 “Pixie-bob Project 2501” ! 🎉 Squeezing more out of every pipeline: compressed results & timeout fixes 🎉 Termination Message Compression The biggest new feature is optional termination message compression ( #9682 ). Kubernetes limits termination messages to 4KB, which constrains how many results a Task step can produce.
