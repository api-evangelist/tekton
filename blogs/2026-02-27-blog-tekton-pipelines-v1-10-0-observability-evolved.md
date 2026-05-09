---
title: "Blog: Tekton Pipelines v1.10.0: Observability, Evolved"
url: "https://tekton.dev/blog/2026/02/27/tekton-pipelines-v1.10.0-observability-evolved/"
date: "2026-02-27"
author: ""
feed_url: "https://tekton.dev/blog/index.xml"
---
We’re excited to announce the release of Tekton Pipelines v1.10.0! The headline for this release is a major infrastructure change: the migration from OpenCensus to OpenTelemetry for all metrics instrumentation. OpenCensus to OpenTelemetry Migration OpenCensus has been deprecated in favor of OpenTelemetry, and Tekton Pipelines now follows suit. This release migrates all PipelineRun and TaskRun metrics to OpenTelemetry instruments — histograms, counters, and gauges — and updates the underlying Knative dependency to v1.19.
