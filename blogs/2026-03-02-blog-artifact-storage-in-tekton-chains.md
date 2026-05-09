---
title: "Blog: Artifact Storage in Tekton Chains"
url: "https://tekton.dev/blog/2026/03/02/artifact-storage-in-tekton-chains/"
date: "2026-03-02"
author: ""
feed_url: "https://tekton.dev/blog/index.xml"
---
Tekton Chains observes TaskRun and PipelineRun executions, captures relevant information, and stores it in a cryptographically-signed format. This post details the supported storage backends and how they organize and persist these artifacts. Where to Keep the Proof? After building a secure pipeline, your images are signed and your build metadata is captured—but where is the signature saved? If you lose the signature, the artifact is as good as unverified. In a secure software supply chain, generating attestations is only half the battle.
