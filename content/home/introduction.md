
+++
title = "Introduction"
description = "Introduction section of slides"
weight = 100
+++

# Introduction

- Whatsamajig?
- Why me? Wherefore?

{{% note %}}


As a community we celebrate individuality, whether it’s your choice of indentation style, yarn vs npm vs pnpm, linting rules, monorepo tools, etc. that’s entirely up to you as an OSS project maintainer, but as an outsider coming in, that’s where it can be a bit more difficult. When someone comes to your repo there’s a process they’ll go through, first they’ll look for and setup instructions in the README file, “what version of Node/dotnet/Python/etc. is required?”, “what package manager(s) are being used?”, “how does one install all the dependencies?”, and so on. Failing that, it’s digging for a contributors guide, whether that’s a CONTRIBUTING.md file, or a page on a wiki, something that’ll help them get started.

All of this starts producing barriers to be able to effectively contribute. Have the wrong version of dotnet and you might not be able to compile. Didn’t realise a linter/formatter was in use can result in a PR failing to meet the code style guide. While dealing with these PR’s as a maintainer is frustrating, it’s equally so for a contributor who has to go back and rework something that they were unaware about to begin with.

Standardising Environments with devcontainers

This is where dev devcontainers come in. A devcontainer is used by the VS Code Remote Containers extension and works by creating a Docker container to do your development in.

As the development environment is within Docker, you supply the Dockerfile and VS Code will take care of building the image and starting the container for you. Then since you control the Dockerfile you can have it install any software you need for your project, set the right version of Node, install global packages, etc.

This is just a plain old Dockerfile, you can run it without VS Code using the standard Docker tools and mount a volume in, but the power comes when you combine it with the devcontainers.json file, which gives VS Code instructions on how to configure itself.

Using eslint + prettier? Tell the devcontainer to install those extensions so the user has them already installed. Want some VS Code settings enabled by default, specify them so users don’t have to know about it.

source: https://www.aaron-powell.com/posts/2021-03-08-your-open-source-project-needs-a-dev-container-heres-why/

{{% /note %}}
