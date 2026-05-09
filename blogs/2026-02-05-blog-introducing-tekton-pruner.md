---
title: "Blog: Introducing Tekton Pruner"
url: "https://tekton.dev/blog/2026/02/05/introducing-tekton-pruner/"
date: "2026-02-05"
author: ""
feed_url: "https://tekton.dev/blog/index.xml"
---
Tekton Pruner automatically cleans up completed PipelineRuns and TaskRuns based on retention policies you define. The Problem Tekton does not delete PipelineRuns and TaskRuns after completion. Over time, this increases etcd storage usage and degrades API performance. Before: Job-Based Pruner The Tekton Operator has a job-based pruner configured via TektonConfig: pruner: disabled: false schedule: "0 8 * * *" startingDeadlineSeconds: 100 # optional resources: - taskrun - pipelinerun keep: 3 # keep-since: 1440 # NOTE: you can use either "keep" or "keep-since", not both prune-per-resource: true…
