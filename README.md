# Golden Owl DevOps Internship Challenge

This document explains the structure and components of the GitHub repository for the Golden Owl DevOps Internship Challenge.

## Repository Overview

The repository is structured to facilitate a hands-on DevOps challenge. The main objective is to provide an environment for learning and demonstrating skills in key DevOps areas such as infrastructure automation, CI/CD pipelines, and monitoring.

### Key Files and Directories

1. **`src/Dockerfile/`**:
   - Contains Dockerfiles and related configurations for containerizing applications.

2. **`.github/workflows/`**:
   - **`pipeline-dev.yml`**:
     - This file defines the CI pipeline for feature branches. It includes jobs for unit testing, SonarQube code analysis, Docker image building, Trivy vulnerability scanning, and deployment to a test environment.
   - **`pipeline-prod.yml`**:
     - This file defines the CD pipeline for the main branch. It deploys the application to the production environment by replacing old Docker containers and verifying the deployment.

### Expected Deliverables
<p align="center">
    <img src="./images/flow_chart.drawio.png" alt="CICD Pipeline" />
<p>
- A fully provisioned infrastructure with the sample application running.
- A working CI/CD pipeline for building, testing, and deploying the application.
- Documentation of steps and any challenges faced during execution.
- **CI/CD Pipeline for Feature Branches**:
  - A fully operational pipeline defined in `pipeline-dev.yml` that automates the following tasks:
    - Unit testing for Node.js.
    - SonarQube code analysis.
    - Docker image building with tagged versions.
    - Vulnerability scanning with Trivy.
    - Deployment to a test environment (EC2).
  - Successful execution of the pipeline for all `feature/*` branches.
- **CD Pipeline for Production**:
  - A production-ready pipeline defined in `pipeline-prod.yml` that automates:
    - Deployment to the production environment (EC2 with load balacner and auto scaling).
  - Successful execution of the pipeline for the `main` branch.

