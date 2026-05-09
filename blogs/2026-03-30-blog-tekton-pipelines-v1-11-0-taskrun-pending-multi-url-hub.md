---
title: "Blog: Tekton Pipelines v1.11.0: TaskRun Pending, Multi-URL Hub Resolver, and PVC Auto-Cleanup"
url: "https://tekton.dev/blog/2026/03/30/tekton-pipelines-v1.11.0-taskrun-pending-multi-url-hub-resolver-and-pvc-auto-cleanup/"
date: "2026-03-30"
author: ""
feed_url: "https://tekton.dev/blog/index.xml"
---
We’re excited to announce the release of Tekton Pipelines v1.11.0 “Javanese Jocasta”! This release focuses on feature parity, resolver improvements, and stability fixes. TaskRun Pending Status TaskRuns now support a pending status, bringing feature parity with PipelineRun. You can create a TaskRun in a pending state and start it later by clearing the spec.status field — useful for scheduling, quota management, or approval gates. apiVersion: tekton.
