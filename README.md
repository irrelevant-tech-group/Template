# Runbook CI/CD Pipeline for <project_name>

In this runbook will be explain everything about the pipeline

## Pre-requisites
### Required Access
- Railway
- Docker hub
- Github (branches)

### Secrets
- DOCKER_USERNAME
- DOCKER_PASSWORD
- RAILWAY_TOKEN

## Procedures (Github actions)

The pipeline is designed to:
- Test branch (build_and_push.yml):
  - Test the code `still on development`
  - Creates the Docker image

- Master branch (deploy.yml):
  - Restart the railway service so the new image is up

### Triggers 
- build_and_push.yml: Push to `tests` branch
- deploy.yml: Push to `master` branch
