
+++
title = "Introduction"
description = "Introduction section of slides"
weight = 100
+++

{{% section %}}

# Introduction

---

## What's the problem?

{{% fragment %}}Dependency hell{{% /fragment %}}
{{% fragment %}}Repo swapping{{% /fragment %}}
{{% fragment %}}Polluted local environments{{% /fragment %}}
{{% fragment %}}Conflicting parallel installs{{% /fragment %}}
{{% fragment %}}Unreproducable results{{% /fragment %}}
{{% fragment %}}Late feedback{{% /fragment %}}
{{% fragment %}}Inconsistent tooling{{% /fragment %}}
{{% fragment %}}Stale documentation{{% /fragment %}}

{{% note %}}

- Dependency hell - solve once and it's done
- Repo swapping - save time on setup, dive into new projects
- Polluted local environments - credentials, environment variables, caches, old versions etc
- Conflicting versions - parallel installations still confusing
- Unreproducable results - don't know what the environment is precisely so can never replicate or trust
- Late feedback - apply tooling early, real-time while editing or pre-commit
- Inconsistent tooling - no more fighting over line endings or formatting rules or linters
- Stale documentation - avoid having to follow x-years-out-of-date Confluence pages about onboarding, new program versions automatically catered for as we've unified documentation and code

{{% /note %}}

---

## What's the solution?

{{% fragment %}}Devcontainers{{% /fragment %}}
{{% fragment %}}Container-based solution{{% /fragment %}}
{{% fragment %}}Options for running{{% /fragment %}}
{{% fragment %}}Lives in-repo{{% /fragment %}}
{{% fragment %}}Optional{{% /fragment %}}
{{% fragment %}}Little to no setup{{% /fragment %}}
{{% fragment %}}Runtime and manager agnostic{{% /fragment %}}
{{% fragment %}}Some limitations{{% /fragment %}}

{{% note %}}

- Devcontainers
- Container-based solution
  - Isolated
  - Familiar technology
  - Can leverage community and developments
  - Lighter than VMs
  - More efficient stacking on hardware
- Options for running - Can run em manually or with VSCode integration
- Lives in-repo alongside the code - everything in the one place
- Optional - not disruptive to existing workflows
- Little to no setup required - minimal system bootstrapping/configuration required, smallest container is one install and one JSON property
- Runtime and manager agnostic - Works with any container runtime/manager
  - Podman for easy rootless
  - Can use other container tools like nerdctl/rancher
  - Works on Docker desktop and Kubernetes (I believe)- Some limitations:
  - Assumptions about host system config files
  - Not as fully featured as Docker naked e.g.: unable to mount secrets at build time
  - No way to share Dockerfiles as libraries (though can use base images + ONBUILD)
  - Sharing cache/envs/config between container and host is a mixed bag

Offhand: Actually JSON5 or something, supports trailing commas and comments, can be a pain for linters

{{% /note %}}

{{% /section %}}

---

## Demo/hands on

Alright, I'll bite. Show me.
