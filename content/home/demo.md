
+++
title = "Demo"
description = "Show using devcontainer and creating"
weight = 200
+++

<!-- I tried using the section code here but it broke the fragments entirely, even the longer syntax -->

# Demonstration

---

## How to use an existing DevContainer

One-time setup:

{{< frag c="1. Install VSCode Remote Containers onto your host" >}}
<br>
{{< frag c="2. Configure a VSCode backend that's capable of running containers" >}}

---

## How to use an existing DevContainer

Every time procedure:

{{< frag c="1. Clone repository and follow the prompt" >}}
<br>
{{< frag c="2. That's it" >}}

---

## In action

- Bare EC2 Ubuntu 20.04
- Bootstrap
  - Config
  - Docker

{{% note %}}
Ubuntu 20.04 is readily available on WSL2, does almost everything satisfactorily, and has broad community support.

Config includes things like Docker and Artifactory credentials, Git config
Docker sortof - I'm using Podman today but they're interchangable for most things at this stage

{{% /note %}}

---

## Anatomy of a devcontainer

- Convention-based
- Only requires image
- Build/Run paradigm
- Compose support

{{% note %}}

- Convention is `.devcontainer/devcontainer.json`
- Can launch any pre-built image from that alone - literally, the only property required is `image` (see )
- Two major separations, build specifications and run specifications
- Can use a Docker Compose file
- Build
  - Build arguments
  - Base image / Dockerfile
  - Build context
  - Caches, targets etc
- Run
  - Volumes/mounts aka disk mapping
  - Environment variables
  - VSCode extensions
  - Features

Microsoft have produced a large range of container images for this purpose, as well as a guided process to produce the accompanying json spec.

You could reference an existing image, local to SilverRail/Artifactory or from the internet, and then just wrap it in a very basic json spec. Alternatively you might clone a repository template for say, dotnet 6 and just get one out the gate for free. Or finally you might simply hit the ol' copy-paste from another repo you've seen.

From scratch is the ultimate in flexibility, it allows you to select build tools and versions expressly and bake in very bespoke configuration and assumptions like repository structure, or module names.
{{% /note %}}
