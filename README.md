<div align="center">
<img src="./assets/logo.png" width="100px" />
</div>

[![CI](https://github.com/jill64/rsac-synchronizer/actions/workflows/ci.yml/badge.svg)](https://github.com/jill64/rsac-synchronizer/actions/workflows/ci.yml)
[![Deploy](https://github.com/jill64/rsac-synchronizer/actions/workflows/deploy.yml/badge.svg)](https://github.com/jill64/rsac-synchronizer/actions/workflows/deploy.yml)

# RSaC Synchronizer

GitHub Repository Settings as Code

## rsac.yaml

```yml
# https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#update-a-repository
repository:
  allow_auto_merge: true

# https://docs.github.com/en/rest/branches/branch-protection?apiVersion=2022-11-28#update-branch-protection
branch-protection:
  - branch-name:
    required_status_checks:
      strict: true
      checks:
        - lint
        - build

#https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#replace-all-repository-topics
topics:
  - topic-name-1
  - topic-name-2
  - topic-name-3

# https://docs.github.com/en/rest/actions/permissions?apiVersion=2022-11-28#set-default-workflow-permissions-for-a-repository
default-workflow-permissions:
  default_workflow_permissions: read
  can_approve_pull_request_reviews: false
```
