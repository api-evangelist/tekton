---
title: "Blog: Tekton Pipelines v1.17.0: Clearer Failures, Sharper Traces"
url: "https://tekton.dev/blog/2026/10/01/tekton-pipelines-v1.17.0-clearer-failures-sharper-traces/"
date: "2026-10-01"
feed_url: "https://tekton.dev/blog/index.xml"
---
We’re excited to announce the release of Tekton Pipelines v1.17.0 “Egyptian Mau Robocop” ! 🎉 Clearer failures, sharper traces 🎉 Surfacing Pod Infrastructure Failures A new alpha feature flag surface-pod-events ( #10690 ) surfaces Pod infrastructure failure reasons — from Warning events such as FailedMount , FailedScheduling , and FailedCreatePodSandBox — directly onto the TaskRun status condition. Previously, a Pod stuck pending for infrastructure reasons produced an unhelpful, generic message.
