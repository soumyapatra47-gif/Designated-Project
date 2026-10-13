# Designated-Project
This is a project almost similar to one I have worked on.

Pipeline Flow

1. Checkout source

   Pulls code from GitHub repository

   Uses stored credentials

   Branch: main

2. Maven Build

   Cleans and builds the project

   Skips tests for faster build

   Generates JAR/WAR in target/

3. SonarQube Scan

   Performs static code analysis

   Checks bugs, smells, vulnerabilities

   Quality gate can be enforced

4. Trivy File Scan

   Scans project files

   Detects security issues

   Finds misconfigs & secrets

5. Docker Build

   Builds Docker image

   Tags image for ECR

   Uses multi-stage build

6. Trivy Image Scan

   Scans Docker Image
   
   Detects OS package vulns
   
   Detects app-level vulns

7. Push image to ECR

   Logs in to Amazon ECR
   
   Tags image for ECR
   
   Pushes image & logs out

8. Deploy to Amazon EKS

   Updates kubeconfig
   
   Updates deployment image
   
   Rolls out new version

9. Verify Deployment

   Checks rollout status

   Lists pods

   Lists services

10. Post Actions

    Sends email on success/failure

    Cleans workspace

    Keeps jenkins tidy
    
