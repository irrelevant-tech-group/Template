# Runbook CI/CD Pipeline for <project_name>

In this runbook will be explain everything about the pipeline

## Pre-requisites
### Required Access
- Docker hub
- Github (branches)

### Secrets
- DOCKER_USERNAME
- DOCKER_PASSWORD

## Procedures (Github actions)

The pipeline is designed to:
- Code in Dev branch:
  - In this branch some test workflows will trigger
  - Merge to production
- When a commit/push is made, a Docker image will be created and pushed into Docker hub

### Triggers 
- tests.yml: Push to `tests` branch
- build_and_push_image.yml: Push to `prod` branch
