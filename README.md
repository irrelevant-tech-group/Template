# Runbook CI/CD Pipeline for <project_name>

In this runbook will be explain everything about the pipeline

## Pre-requisites
### Required Access
- Docker hub
- Github (branches)

### Secrets
- DOCKER_USERNAME
- DOCKER_PASSWORD

## Pipeline

The pipeline is designed to:
- Code in `dev` branch:
  - In this branch some test workflows will trigger
- Merge to `prod`branch
  - When a commit/push is made, a Docker image will be created and pushed into Docker hub

### Triggers 
- tests.yml: Push to `dev` branch
- build_and_push_image.yml: Push to `prod` branch
