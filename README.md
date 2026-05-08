# Tekton (tekton)

Tekton is a cloud-native CI/CD framework implemented as a set of Kubernetes Custom Resource Definitions and controllers under the tekton.dev API group. Tekton is a CNCF Incubating project, licensed under Apache 2.0.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/tekton/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=tekton-api-evangelist&utm_content=repo)

## Type

- **x-type:** opensource (CNCF Incubating, Apache License 2.0)

## Tags

 - DevOps, CI/CD, Kubernetes, CNCF, Pipelines, Open Source, CRD, Operator

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## APIs

| API | Description |
|---|---|
| Tekton Task CRD | tekton.dev/v1 kind=Task |
| Tekton TaskRun CRD | tekton.dev/v1 kind=TaskRun |
| Tekton Pipeline CRD | tekton.dev/v1 kind=Pipeline |
| Tekton PipelineRun CRD | tekton.dev/v1 kind=PipelineRun |
| Tekton ClusterTask CRD | cluster-scoped Task (deprecated for resolvers) |
| Tekton StepAction CRD | reusable parameterizable step |
| Tekton CustomRun CRD | extension point for custom controllers |
| Tekton Resolver Framework | Git/Hub/Bundles/Cluster/HTTP remote resolution |
| Tekton EventListener CRD | webhook sink for Triggers |
| Tekton Trigger CRD | binding + template + interceptors |
| Tekton TriggerBinding CRD | extracts fields from event payloads |
| Tekton TriggerTemplate CRD | declares run resources |
| Tekton ClusterInterceptor CRD | pluggable webhook handlers |
| Tekton Results API | gRPC + REST history store for runs and logs |
| Tekton Chains | signed in-toto / SLSA provenance |
| Tekton Pipelines as Code | Git-native CI/CD on PR/push |
| Tekton Dashboard API | thin proxy/HTTP API for the UI |
| Tekton CLI (tkn) | official command-line tool |
| Tekton Operator CRDs | TektonConfig, TektonPipeline, etc. |
| Tekton Hub API | catalog of reusable Tasks and Pipelines |
| Tekton Catalog | curated community Tasks and Pipelines |

## Common Properties

- [Website](https://tekton.dev/)
- [Documentation](https://tekton.dev/docs/)
- [GitHub Organization](https://github.com/tektoncd)
- [Source (pipeline)](https://github.com/tektoncd/pipeline)
- [License (Apache 2.0)](https://github.com/tektoncd/pipeline/blob/main/LICENSE)
- [CNCF Project](https://www.cncf.io/projects/tekton/)
- [Hub](https://hub.tekton.dev/)
- [Plans](plans/tekton-plans-pricing.yml) — API Commons Plans 0.1 (FOSS — no commercial billing)
- [RateLimits](rate-limits/tekton-rate-limits.yml) — API Commons Rate Limits 0.1 (operator-tuned)
- [FinOps](finops/tekton-finops.yml) — FOCUS-aligned (FOSS — no commercial billing)

## Plans Summary

- **Open Source (Apache 2.0)** — free, CNCF Incubating, all components included
- **Third-Party Distributions** — Red Hat OpenShift Pipelines, IBM Cloud Continuous Delivery, Pipelines-as-Code on cloud platforms (out of scope of this profile)

## Rate Limits Summary

- **Controller QPS to Kubernetes API:** default 50 (tunable)
- **Controller burst:** default 50 (tunable)
- **Concurrent PipelineRuns:** unlimited; bound via Kubernetes ResourceQuotas
- **EventListener throughput:** sized by Sink replicas + ingress
- **Kubernetes API Priority and Fairness (APF)** governs cluster-side rate limiting

## Artifacts

| Artifact | Path |
|---|---|
| Plans | `plans/tekton-plans-pricing.yml` |
| Rate Limits | `rate-limits/tekton-rate-limits.yml` |
| FinOps | `finops/tekton-finops.yml` |

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
