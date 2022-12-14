# Azure DevOps YAML Pipelines - Personal Learning Notes

## Resources
- [LinkedIn - Azure DevOps: Continuous Delivery with YAML Pipelines](https://www.linkedin.com/learning/azure-devops-continuous-delivery-with-yaml-pipelines/)
  - [Pipeline - Key Concepts - Diagram - 3:39](https://www.linkedin.com/learning/azure-devops-continuous-delivery-with-yaml-pipelines/azure-pipelines-core-concepts?autoplay=true&resume=false)
  - [CI Pipeline -> CD Pipeline -> IIS 0:00](https://www.linkedin.com/learning/azure-devops-continuous-delivery-with-yaml-pipelines/continuous-integration-pipelines?autoplay=true&resume=false)
  - [Pipeline - In-line PS script - Example - 3:18](https://www.linkedin.com/learning/azure-devops-continuous-delivery-with-yaml-pipelines/yaml-pipeline-basics?autoplay=true&resume=false)  
  - [Pipeline - Classic to YAML - Mapping - 4:08](https://www.linkedin.com/learning/azure-devops-continuous-delivery-with-yaml-pipelines/yaml-pipeline-basics?autoplay=true&resume=false)
  - [Add build number using Replace Tokens task - 0:00](https://www.linkedin.com/learning/azure-devops-continuous-delivery-with-yaml-pipelines/customizing-the-workflow?autoSkip=true&autoplay=true&resume=false)
  - [Azure WebApp Deployment - YAML Example - Part 1 - 1:21](https://www.linkedin.com/learning/azure-devops-continuous-delivery-with-yaml-pipelines/customizing-the-workflow?autoSkip=true&autoplay=true&resume=false)
  - [Azure WebApp Deployment - YAML Example - Part 2 - 0:00](https://www.linkedin.com/learning/azure-devops-continuous-delivery-with-yaml-pipelines/deploying-code?autoSkip=true&autoplay=true&resume=false)

## Azure DevOps
- New version of TFS (Team Foundation Server)
- Available both on-premises (Azure DevOps Server) and in the cloud

## Azure DevOps - Features]
- Boards
- Repositories
- Pipelines
- Test Plans
- Artifacts

## Pipelines - Hierachy
- Trigger
- Stages
  - Jobs (run on an agent in  a pool)
    - Steps (Tasks and Scripts)

## Build Pipeline VS Release Pipeline
- Build Pipeline produces artifacts
- Artificats creation may trigger Release Pipeline ...
- ... or Release Pipeline may be time-based scheduled

## Continuous Integration Build (CI Build)
- Simplify and automate testing and building of code
- Catch bugs early in development cycle
- Can be scheduled or triggered by code changes
- Produce items knows as build artifacts
- Should be fast and easy to run
- Automated running of unit tests

## Continuous Delivery Build (CD Build)
- Automatically deploy code to environments
  - Development/testing/staging/production
- Triggers can include artifacts being published as well as time-based scheduled releases
- Use tested code from CI process
- Implemented as **Deployment Jobs**

## Deployment Jobs
- Special jobs that publish code to machines
- Collection of steps to run sequentially against an environment
  - `AzureRmWebAppDeployment`
  - Web Deploy
  - Kubernetes
  - VM
  - More ...

## Build Artifacts
- Output of a build
- May be one or more files
- Typically used in continuous delivery
