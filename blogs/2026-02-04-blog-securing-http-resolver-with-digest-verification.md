---
title: "Blog: Securing HTTP Resolver with Digest Verification"
url: "https://tekton.dev/blog/2026/02/04/securing-http-resolver-with-digest-verification/"
date: "2026-02-04"
author: ""
feed_url: "https://tekton.dev/blog/index.xml"
---
Overview When fetching remote resources like Tasks and Pipelines from HTTP URLs for your PipelineRun, there’s always a risk that the content could be tampered with during transit or at the source. To address this security concern, the Tekton HTTP resolver now supports optional digest validation, allowing users to verify the integrity of fetched content against a known cryptographic hash. This feature enables users to specify an expected digest (SHA256 or SHA512) in their PipelineRun definitions.
