# Tekton (tekton)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Tekton is a cloud-native CI/CD framework implemented as a set of Kubernetes Custom Resource Definitions and controllers under the tekton.dev API group. Tekton is a CNCF Incubating project. Its primary API surface is Kubernetes-native — Tasks, Pipelines, PipelineRuns, TaskRuns, EventListeners, Triggers, etc. — accessed through the Kubernetes API server (kubectl, client-go, the tkn CLI, and the Tekton Dashboard). Tekton itself is open-source under Apache 2.0; commercial offerings layered on Tekton (Red Hat OpenShift Pipelines, Jenkins X, Google Cloud Build private preview integrations, IBM Cloud Continuous Delivery, Pipelines-as-Code on GitOps platforms) are out of scope of the upstream project.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/tekton/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tekton/refs/heads/main/apis.yml)

## Tags

- DevOps
- CI/CD
- Kubernetes
- CNCF
- Pipelines
- Open Source
- CRD
- Operator

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## APIs

### Tekton Task CRD

tekton.dev/v1 kind=Task — defines a series of steps that launch specific build or delivery tools, ingest specific inputs (params, workspaces, resources), and produce specific outputs (results). Tasks are the reusable unit of execution in Tekton.

#### Tags

- CRD
- Tasks
- Steps
- Build

#### Properties

- [Documentation](https://tekton.dev/docs/pipelines/tasks/)
- [Source](https://github.com/tektoncd/pipeline/blob/main/config/300-task.yaml)
- [OpenAPI](openapi/tekton-pipeline-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton TaskRun CRD

tekton.dev/v1 kind=TaskRun — instantiates a Task with specific inputs, workspace bindings, and execution parameters. The TaskRun controller runs the steps as Kubernetes pods and surfaces status, logs, and results.

#### Tags

- CRD
- TaskRuns
- Execution

#### Properties

- [Documentation](https://tekton.dev/docs/pipelines/taskruns/)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Pipeline CRD

tekton.dev/v1 kind=Pipeline — defines an ordered/parallelized series of Tasks that accomplish a specific build or delivery goal. Pipelines compose Tasks via params, workspaces, results, and finally tasks.

#### Tags

- CRD
- Pipelines
- Workflows

#### Properties

- [Documentation](https://tekton.dev/docs/pipelines/pipelines/)
- [Source](https://github.com/tektoncd/pipeline/blob/main/config/300-pipeline.yaml)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton PipelineRun CRD

tekton.dev/v1 kind=PipelineRun — instantiates a Pipeline with specific param values, workspace bindings, service accounts, and timeouts. The PipelineRun controller orchestrates the underlying TaskRuns.

#### Tags

- CRD
- PipelineRuns
- Execution

#### Properties

- [Documentation](https://tekton.dev/docs/pipelines/pipelineruns/)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton ClusterTask CRD

tekton.dev/v1beta1 kind=ClusterTask — cluster-scoped variant of Task, allowing a single definition to be referenced from any namespace. Marked deprecated in favor of remote resolution but still widely used.

#### Tags

- CRD
- ClusterTasks
- Cluster-Scoped

#### Properties

- [Documentation](https://tekton.dev/docs/pipelines/tasks/#tekton-clustertasks)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton StepAction CRD

tekton.dev/v1beta1 kind=StepAction — reusable, parameterizable step definition that can be referenced from multiple Tasks, enabling tighter sharing than copy-pasting step blocks.

#### Tags

- CRD
- StepActions
- Reusable

#### Properties

- [Documentation](https://tekton.dev/docs/pipelines/stepactions/)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton CustomRun CRD

tekton.dev/v1beta1 kind=CustomRun — generic execution resource that custom controllers reconcile, enabling third-party orchestrators to extend Tekton with non-Pod-based execution semantics.

#### Tags

- CRD
- CustomRun
- Extension

#### Properties

- [Documentation](https://tekton.dev/docs/pipelines/customruns/)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Resolver Framework

The Tekton Resolution API (tekton.dev/v1alpha1 kind=ResolutionRequest) and built-in resolvers (Git, Hub, Bundles, Cluster, HTTP) fetch Tasks and Pipelines from remote sources at run time, so PipelineRuns can reference versioned remote definitions without bundling them in-cluster.

#### Tags

- Resolution
- Resolvers
- Remote

#### Properties

- [Documentation](https://tekton.dev/docs/pipelines/resolution/)
- [Source](https://github.com/tektoncd/pipeline/tree/main/pkg/resolution)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton EventListener CRD

triggers.tekton.dev/v1beta1 kind=EventListener — runs an HTTP server (Sink) that receives webhooks (e.g., GitHub push events), applies interceptors, and creates Pipeline/TaskRun objects via TriggerTemplates.

#### Tags

- CRD
- EventListener
- Triggers
- Webhooks

#### Properties

- [Documentation](https://tekton.dev/docs/triggers/eventlisteners/)
- [Source](https://github.com/tektoncd/triggers)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Trigger CRD

triggers.tekton.dev/v1beta1 kind=Trigger — combines TriggerBindings (extracting fields from incoming events) and a TriggerTemplate (instantiating PipelineRuns/TaskRuns) used by EventListeners.

#### Tags

- CRD
- Trigger
- TriggerBinding
- TriggerTemplate

#### Properties

- [Documentation](https://tekton.dev/docs/triggers/triggers/)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton TriggerBinding CRD

triggers.tekton.dev/v1beta1 kind=TriggerBinding (and ClusterTriggerBinding) — extracts fields from event payloads and binds them to params used by TriggerTemplates.

#### Tags

- CRD
- TriggerBinding

#### Properties

- [Documentation](https://tekton.dev/docs/triggers/triggerbindings/)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton TriggerTemplate CRD

triggers.tekton.dev/v1beta1 kind=TriggerTemplate — declares the PipelineRun/TaskRun resources that should be instantiated when a matching event is received, parameterized by TriggerBindings.

#### Tags

- CRD
- TriggerTemplate

#### Properties

- [Documentation](https://tekton.dev/docs/triggers/triggertemplates/)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton ClusterInterceptor CRD

triggers.tekton.dev/v1alpha1 kind=ClusterInterceptor (and namespace-scoped Interceptor) — pluggable webhook handler that filters, validates, and mutates incoming events before they reach a TriggerTemplate (built-in interceptors include GitHub, GitLab, Bitbucket, CEL).

#### Tags

- CRD
- Interceptor
- Filtering

#### Properties

- [Documentation](https://tekton.dev/docs/triggers/clusterinterceptors/)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Results API

Tekton Results provides a long-term store and a gRPC + REST API for completed PipelineRun/TaskRun records and their logs, freeing the Kubernetes etcd from acting as a CI history database.

#### Tags

- Results
- History
- Storage
- GRPC

#### Properties

- [Documentation](https://tekton.dev/docs/results/)
- [Source](https://github.com/tektoncd/results)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Chains

Tekton Chains observes completed TaskRuns/PipelineRuns and emits signed in-toto/SLSA provenance attestations to OCI registries, transparency logs (Rekor), or storage backends — supplying the supply-chain integrity surface for Tekton CI/CD.

#### Tags

- Supply Chain
- Provenance
- SLSA
- Signing

#### Properties

- [Documentation](https://tekton.dev/docs/chains/)
- [Source](https://github.com/tektoncd/chains)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Pipelines as Code

Pipelines as Code lets you store Tekton Pipeline definitions inside the same Git repository as your application code (.tekton/) and runs them on PR/push events from GitHub/GitLab/Bitbucket/Gitea, providing a Git-native CI/CD experience.

#### Tags

- Pipelines as Code
- GitOps
- GitHub
- GitLab

#### Properties

- [Documentation](https://tekton.dev/docs/pipelinesascode/)
- [Source](https://github.com/openshift-pipelines/pipelines-as-code)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Dashboard API

The Tekton Dashboard exposes a web UI and a thin proxy/HTTP API over the Tekton CRDs and Tekton Results, providing browsing, log streaming, and run management capabilities.

#### Tags

- Dashboard
- UI
- Backend

#### Properties

- [Documentation](https://tekton.dev/docs/dashboard/)
- [Source](https://github.com/tektoncd/dashboard)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton CLI (tkn)

tkn is the official Tekton command-line tool wrapping the Kubernetes API for Tekton resources — start runs, stream logs, list/describe Tasks and Pipelines, manage triggers, and bootstrap projects.

#### Tags

- CLI
- tkn
- Operations

#### Properties

- [Documentation](https://tekton.dev/docs/cli/)
- [Source](https://github.com/tektoncd/cli)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Operator CRDs

operator.tekton.dev kinds (TektonConfig, TektonPipeline, TektonTrigger, TektonChain, TektonHub, TektonAddon, TektonDashboard, TektonResult) — the Tekton Operator installs and lifecycle-manages all Tekton subprojects on a cluster.

#### Tags

- CRD
- Operator
- Lifecycle
- TektonConfig

#### Properties

- [Source](https://github.com/tektoncd/operator)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Hub API

Tekton Hub is a public catalog of reusable Tasks and Pipelines exposed via REST API — search, fetch, and resolve community-published resources for use via the Hub resolver.

#### Tags

- Hub
- Catalog
- Discovery

#### Properties

- [Documentation](https://hub.tekton.dev/)
- [Source](https://github.com/tektoncd/hub)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Tekton Catalog

The Tekton Catalog hosts community-curated, versioned Task and Pipeline definitions consumed via the Hub or directly by the Git resolver.

#### Tags

- Catalog
- Library
- Reusable

#### Properties

- [Source](https://github.com/tektoncd/catalog)
- [Postman Collection](collections/tekton-pipeline.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tekton-pipeline.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://tekton.dev/)
- [Documentation](https://tekton.dev/docs/)
- [Getting Started](https://tekton.dev/docs/getting-started/)
- [GitHub Organization](https://github.com/tektoncd)
- [Source](https://github.com/tektoncd/pipeline)
- [Triggers](https://github.com/tektoncd/triggers)
- [Chains](https://github.com/tektoncd/chains)
- [Results](https://github.com/tektoncd/results)
- [Operator](https://github.com/tektoncd/operator)
- [C L I](https://github.com/tektoncd/cli)
- [Dashboard](https://github.com/tektoncd/dashboard)
- [Catalog](https://github.com/tektoncd/catalog)
- [Hub](https://hub.tekton.dev/)
- [License](https://github.com/tektoncd/pipeline/blob/main/LICENSE)
- [C N C F  Project](https://www.cncf.io/projects/tekton/)
- [Slack  Community](https://tektoncd.slack.com/)
- [Blog](https://tekton.dev/blog/)
- [X ( Twitter)](https://x.com/tektoncd)
- [YouTube](https://www.youtube.com/c/TektonCD)
- [Releases](https://github.com/tektoncd/pipeline/releases)
- [Roadmap](https://github.com/tektoncd/pipeline/blob/main/roadmap.md)
- [Plans](plans/tekton-plans-pricing.yml)
- [Rate Limits](rate-limits/tekton-rate-limits.yml)
- [Fin Ops](finops/tekton-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
