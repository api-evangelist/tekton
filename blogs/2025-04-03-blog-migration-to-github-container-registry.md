---
title: "Blog: Migration to Github Container Registry"
url: "https://tekton.dev/blog/2025/04/03/migration-to-github-container-registry/"
date: "2025-04-03"
author: ""
feed_url: "https://tekton.dev/blog/index.xml"
---
Why and How Dear Tekton users and contributors, to reduce costs, we’ve migrated all our releases to the free tier on ghcr.io/tektoncd. All new Tekton releases are exclusively on ghcr.io/tektoncd. Old releases are also now available on ghcr.io/tektoncd. Please migrate your old releases to ghcr.io immediately since we have limited funding to allocate to gcr.io egress. To migrate you need to replace gcr.io/tekton-releases with ghcr.io/tektoncd in all your images including all image references in the manifests, not only those that specify the image of the deployment, e.g.
