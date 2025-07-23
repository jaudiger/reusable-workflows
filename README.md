# Reusable Workflows

## Instructions

This repository holds all the reusable GitHub Actions workflows that I'm using in my projects hosted on GitHub. I could also create my own GitHub Actions to be then called from other repositories, but I prefer to use this approach to have a centralized place to manage and update my workflows.

Calling workflows from other repositories is as simple as:

```yaml
jobs:
  call-workflow:
    uses: jaudiger/reusable-workflows/.github/workflows/call-workflow.yml@ref
    secrets: inherit
```

## CI / CD

The CI/CD pipeline is configured using GitHub Actions. The workflow is defined in the [`.github/workflows`](.github/workflows) folder:

- Static Analysis

Additionally, Dependabot is configured to automatically update dependencies (GitHub Actions, Terraform providers, Cargo dependencies).

## Repository configuration

The settings of this repository are managed from the [gitops-deployments](https://github.com/jaudiger/gitops-deployments) repository using Terraform. The actual configuration applied is located in the Terraform module [`modules/github-repository`](https://github.com/jaudiger/gitops-deployments/tree/main/modules/github-repository).
