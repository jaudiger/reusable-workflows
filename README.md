# Reusable Workflows

## Getting Started

This repository holds all the reusable GitHub Actions workflows that I'm using in my projects hosted on GitHub. I could also create my own GitHub Actions to be then called from other repositories, but I prefer to use this approach to have a centralized place to manage and update my workflows.

Calling workflows from other repositories is as simple as:

```yaml
jobs:
  call-workflow:
    uses: jaudiger/reusable-workflows/.github/workflows/call-workflow.yml@ref
    secrets: inherit
```
