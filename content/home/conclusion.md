
+++
title = "Conclusion"
description = "Wrap up and feedback"
weight = 300
+++

## Conclusion

{{< frag c="I love containers" >}}
{{< frag c="and so will you" >}}
<br>
{{< frag c="this is a threat" >}}
{{< frag c="🙃" >}}

{{% note %}}

Devcontainers are awesome, we can use them to define an isolated development environment within Docker that has all that we need, and only what we need, installed in it. This helps simplify people getting into a new codebase by removing the barrier of unknown around what to setup before then can start working. Using the same container that your application ships in, or runs its CI jobs in, or tests in, can make debugging _extremely_ effective. While I talked about this from the standpoint of OSS, the same pattern can be applied to internal company projects. You don’t even have to ship a Dockerfile, you can point the devcontainer.json to a Docker image and speed up the process.

Open the floor to plenary questions/comments/discussion

{{% /note %}}

---

## Resources

- [Remote containers development](https://code.visualstudio.com/docs/remote/containers)
- [Devcontainer JSON spec](https://containers.dev/implementors/json_reference/)
- [Sample JSONs](https://gitlab-bne.silverrail.io/brisbane-office/shared-libraries/file-templates/-/tree/master/.devcontainer)
- [This presentation (repo)](https://gitlab-bne.silverrail.io/brisbane-office/labs/demos/devcontainers)
- [This presentation (site)](https://brisbane-office.pages-bne.silverrail.io/labs/demos/devcontainers)
<br>
<br>
[Return to start](#starting-slide)
