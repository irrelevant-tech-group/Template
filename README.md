# Repository Standards

## Naming Convension

- Divide the name in min 2 parts:
  - First one must be the hiring company name
  - Second name could be:
     - Type of develpment (Web Development, Mobile Development, API Development)
     - Type of service (Support Services, Consulting Services, Maintenance Services, Integration Services)


# Runbook CI/CD Pipeline for project

In this runbook will be explain everything about the pipeline of the code for the project

## Pre-requisites

### Required Access
- Docker hub
- Github (branches)

### Variables
- REPO_NAME

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
