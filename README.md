# DevContainer Presentation

Repository template for DevContainer presentation

## Viewing

Go to the GitLab pages URL and view the presentation.

## Delivering

### Preparation

1. Locate [Ubuntu AMI](https://cloud-images.ubuntu.com/locator/ec2/)
1. Fire up WSL2 Ubuntu
1. Create EC2 instance and get IP
    `export IP=`
1. SSH key copy
   `scp $HOME/.ssh/* ubuntu@$IP:~/.ssh`
1. SSH using private IP (note that our VPN is now properly configured for this)
    `ssh ubuntu@$IP`
1. Set up a dotnet 6 repository

    ```Bash
    git clone git@gitlab-bne.silverrail.io:brisbane-office/seat-selector/seat-map-service.git
    cd seat-map-service
    git checkout ft-gitlab-pipelines
    ```

1. Set up a Ruby repo
   `git clone git@gitlab-bne.silverrail.io:brisbane-office/shared-libraries/repository-templates/ruby-gem.git`
1. Set up Python repo

    ```Bash
    git clone https://github.com/arichtman/gitlab-lint.git
    cd gitlab-lint
    git switch ft-domain-validation
    ```

1. Configure VSCode remote to the instance
1. Open a window connnected to the instance
1. DO NOT BOOTSTRAP anything else
