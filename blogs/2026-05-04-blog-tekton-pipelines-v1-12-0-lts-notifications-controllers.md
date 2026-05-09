---
title: "Blog: Tekton Pipelines v1.12.0 LTS: Notifications Controllers, Security Hardening, and Performance"
url: "https://tekton.dev/blog/2026/05/04/tekton-pipelines-v1.12.0-lts-notifications-controllers-security-hardening-and-performance/"
date: "2026-05-04"
author: ""
feed_url: "https://tekton.dev/blog/index.xml"
---
We’re excited to announce the release of Tekton Pipelines v1.12.0 “Exotic Shorthair Elektrobots LTS”! This is a Long Term Support (LTS) release, supported until May 2027. TEP-0137: Notifications Controllers The headline feature of v1.12.0 is the implementation of TEP-0137 — dedicated notifications controllers for PipelineRun and TaskRun CloudEvents. What Changed CloudEvents for PipelineRuns and TaskRuns are now sent by a dedicated tekton-events-controller deployment, rather than being embedded in the PipelineRun and TaskRun reconcilers.
