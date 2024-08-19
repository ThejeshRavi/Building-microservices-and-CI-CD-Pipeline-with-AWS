**Overview:**
This project focuses on transitioning a monolithic application to a microservices architecture using AWS services, setting up a CI/CD pipeline, Dockerizing the microservices, and deploying them on Amazon ECS with a blue/green deployment strategy.

### **Phase 1: Infrastructure Analysis**
- Conducted an analysis of the existing monolithic application's infrastructure:
  - Hosted on an Amazon EC2 instance with HTTP access.
  - Utilizes a Node.js server running on port 80.
  - Stores data in MySQL on Amazon RDS.
  - Identified necessary URLs and the basic RESTful structure for CRUD operations.
  - Prepared the system for transitioning to a microservices architecture.

### **Phase 2: Development Environment Setup**
- Created an AWS Cloud9 IDE for development.
- Established SSH access and migrated the source code of the monolithic application.
- Organized directories for the customer and employee microservices.
- Initialized a Git repository (CodeCommit) for version control.
- Laid the groundwork for the future microservices architecture.

### **Phase 3: Microservices Dockerization**
- Configured Docker containers for the customer and employee microservices.
- Independently tested each microservice using Docker on ports 8080 and 8081.
- Prepared Docker images for deployment on ECS.
- Integrated the Docker workflow with Git (CodeCommit) for version control.

### **Phase 4: ECS Infrastructure Setup**
- Created Amazon ECR repositories to store Docker images.
- Set up an ECS cluster using AWS Fargate to ensure scalability.
- Defined ECS task definitions and AppSpec files for CodeDeploy.
- Configured the environment for future automated deployments.

### **Phase 5: Application Load Balancer Configuration**
- Implemented an Application Load Balancer with path-based routing.
- Set up a blue/green deployment strategy to minimize downtime during updates.
- Managed target groups for the customer and employee microservices.
- Ensured proper traffic routing and security configurations.

### **Phase 6: ECS Service Creation**
- Established ECS services for the customer and employee microservices.
- Linked these services to their respective task definitions and target groups.
- Prepared the system for the independent deployment and scaling of each microservice.

### **Phase 7: CI/CD Pipeline Implementation**
- Configured a CodeDeploy application to handle microservices deployments.
- Set up CodePipeline for continuous integration and deployment.
- Automated Docker image updates to trigger CodeDeploy deployments.
- Verified successful deployments and traffic rerouting during updates.

### **Phase 8: Scaling and Security Enhancements**
- Restricted access to the employee microservice based on IP address.
- Updated the UI for the employee microservice and pushed changes to ECR.
- Triggered CodePipeline to deploy the updated microservices.
- Scaled the customer microservice by adjusting container counts.
- Tested access controls and ensured the system's scalability.

Conclusion:
This is an overview of each project phase, detailing setup, configurations, and achievements. It serves as a guide for understanding the project's evolution from a monolithic application to a scalable microservices architecture on AWS.
