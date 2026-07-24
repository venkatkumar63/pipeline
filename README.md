# CI/CD Pipeline with AWS CodePipeline, CodeBuild, and CodeDeploy

## Project Overview
This project demonstrates how to build a Continuous Integration and Continuous Deployment (CI/CD) pipeline using AWS services. The pipeline automatically builds, tests, and deploys a web application to an Amazon EC2 instance running Apache.

## Architecture

GitHub
   ↓
AWS CodePipeline
   ↓
AWS CodeBuild
   ↓
Amazon S3 (Artifact Storage)
   ↓
AWS CodeDeploy
   ↓
Amazon EC2 (Apache Web Server)

## Technologies Used

- Git & GitHub
- AWS CodePipeline
- AWS CodeBuild
- AWS CodeDeploy
- Amazon EC2
- Amazon S3
- IAM
- Apache HTTP Server
- Linux (Amazon Linux 2)

## Prerequisites

- AWS Account
- IAM Role with required permissions
- EC2 Instance
- CodeDeploy Agent installed
- Apache Web Server installed
- Git installed

## Project Structure

```
project/
├── appspec.yml
├── index.html
├── scripts/
│   ├── install_dependencies.sh
│   ├── start_server.sh
│   └── stop_server.sh
└── README.md
```

## Deployment Steps

1. Create a GitHub repository.
2. Upload the project files.
3. Create an S3 bucket for artifacts.
4. Create a CodeDeploy application.
5. Create a Deployment Group.
6. Create a CodeBuild project.
7. Create a CodePipeline.
8. Push changes to GitHub.
9. CodePipeline automatically builds and deploys the application.

## Verification

After successful deployment:

- Open the EC2 Public IP in your browser.
- Verify the application is running.

Example:

```
http://<EC2-Public-IP>
``
