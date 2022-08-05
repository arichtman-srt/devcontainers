
+++
title = "Demo"
description = "Show using devcontainer and creating"
weight = 200
+++

## Using an existing DevContainer

{{< frag c="0. Clone repository" >}}
<br>
{{< frag c="1. That's it" >}}

---

# Showtime

{{% note %}}
1. Show Ubuntu 22.04 machine, explain it's barely bootstrapped with container runtime, SSH keys, some Artifactory authentication bits
1. Show that we have no dotnet, 
1. run `code repos/


{{% /note %}}

---

## Creating DevContainers

- Samples with guidance
- Copy existing
- From scratch

{{% note %}}
Microsoft have produced a large range of container images for this purpose, as well as a guided process to produce the accompanying json spec.

You could reference an existing image, local to SilverRail/Artifactory or from the internet, and then just wrap it in a very basic json spec. Alternatively you might clone a repository template for say, dotnet 6 and just get one out the gate for free. Or finally you might simply hit the ol' copy-paste from another repo you've seen.

From scratch is the ultimate in flexibility, it allows you to select build tools and versions expressly and bake in very bespoke configuration and assumptions like repository structure, or module names.
{{% /note %}}
