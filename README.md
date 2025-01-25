# AWS Microservices Project README

## Overview
This project aims to transition a monolithic application into microservices architecture using AWS services. It involves setting up a CI/CD pipeline, Dockerizing microservices, and deploying them on Amazon ECS with blue/green deployment strategies.

### Phase 1: Analyzing the Infrastructure
In this phase, the current monolithic application's infrastructure was analyzed:
- Hosted on an Amazon EC2 instance accessible via HTTP.
- Uses Node.js server on port 80.
- Data stored in MySQL on Amazon RDS.
- Identified URLs and basic RESTful structure for CRUD operations.
- Prepared for transition to microservices.

### Phase 2: Setting up Development Environment
- Created AWS Cloud9 IDE for development.
- Established SSH access and copied monolithic app source code.
- Organized directories for customer and employee microservices.
- Initialized Git repository (CodeCommit) for version control.
- Prepared for future microservices architecture.

### Phase 3: Dockerizing Microservices
- Configured Docker containers for customer and employee microservices.
- Tested each microservice independently using Docker on ports 8080 and 8081.
- Prepared Docker images for ECS deployment.
- Integrated Docker workflow with Git (CodeCommit).

### Phase 4: ECS Infrastructure Setup
- Created Amazon ECR repositories for Docker images.
- Set up ECS cluster using AWS Fargate for scalability.
- Defined ECS task definitions and AppSpec files for CodeDeploy.
- Configured for future automated deployments.

### Phase 5: Application Load Balancer Setup
- Implemented Application Load Balancer with path-based routing.
- Configured blue/green deployment strategy for minimal downtime.
- Managed target groups for customer and employee microservices.
- Ensured proper traffic routing and security group configurations.

### Phase 6: Creating ECS Services
- Established ECS services for customer and employee microservices.
- Linked ECS services to respective task definitions and target groups.
- Prepared for independent deployment and scaling of microservices.

### Phase 7: CI/CD Pipeline with CodeDeploy
- Configured CodeDeploy application for microservices deployment.
- Set up CodePipeline for continuous integration and deployment.
- Automated Docker image updates triggering CodeDeploy deployments.
- Verified deployment and traffic rerouting during updates.

### Phase 8: Scaling and Security Adjustments
- Limited access to employee microservice based on IP address.
- Updated UI for employee microservice and pushed changes to ECR.
- Triggered CodePipeline to deploy updated microservices.
- Scaled customer microservice by adjusting container counts.
- Tested access controls and scalability features.

## Conclusion
This README provides an overview of each project phase, detailing setup, configurations, and achievements. It serves as a guide for understanding the project's evolution from a monolithic application to a scalable microservices architecture on AWS.
