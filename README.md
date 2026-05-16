# AWS Lambda CI/CD Pipeline with GitHub Actions

## Overview

This project demonstrates a CI/CD pipeline for deploying and validating AWS infrastructure and AWS Lambda functions using GitHub Actions.

The main goal of the project is to practice DevOps automation, Infrastructure as Code (IaC), and cloud deployment workflows in AWS.

The repository includes:

- AWS Lambda deployment automation
- GitHub Actions CI/CD workflows
- CloudFormation template validation
- Automated AWS infrastructure deployment
- Pull Request-based testing workflow
- Stack cleanup automation

---

# Technologies Used

- AWS Lambda
- AWS CloudFormation
- GitHub Actions
- Python
- YAML
- AWS CLI
- Git & GitHub

---

# Project Architecture

```text
Developer Push / Pull Request
            │
            ▼
     GitHub Actions Workflow
            │
 ┌──────────┴──────────┐
 │                     │
 ▼                     ▼
Validate CloudFormation   Deploy Lambda Function
 │                     │
 ▼                     ▼
Create Test Stack     Update AWS Lambda
 │
 ▼
Comment PR with Deployment Info
 │
 ▼
Cleanup Stack After Merge
```

---

# Features

## AWS Lambda CI/CD Deployment

- Automatically deploys AWS Lambda functions on push events
- Uses GitHub Actions workflows
- Packages Lambda code dynamically
- Updates Lambda functions using AWS CLI

---

## CloudFormation Validation Pipeline

- Validates CloudFormation templates automatically
- Creates temporary AWS test stacks during Pull Requests
- Uses parameterized environments
- Supports automated cleanup after merge

---

## Pull Request Automation

- PR-triggered infrastructure validation
- Automated deployment feedback comments
- Temporary test environment provisioning

---

# Repository Structure

```text
lambda-cicd/
│
├── .github/workflows/
│   ├── lambda.yml
│   └── cfn-validate-pr.yml
│
├── cloudformation/
│   └── s3-bucket.yml
│
├── lambda/
│   ├── lambda_function.py
│   └── requirements.txt
│
└── README.md
```

---

# CI/CD Workflow Details

## Lambda Deployment Workflow

The Lambda deployment workflow:

1. Triggers on push to the main branch
2. Sets up Python environment
3. Installs dependencies
4. Configures AWS credentials
5. Packages Lambda source code
6. Deploys updated Lambda function to AWS

---

## CloudFormation PR Validation Workflow

The CloudFormation validation workflow:

1. Triggers on Pull Requests
2. Validates CloudFormation templates
3. Deploys temporary AWS test stack
4. Adds deployment information to the PR
5. Deletes temporary stack after merge

---

# Example AWS Services Used

- AWS Lambda
- AWS CloudFormation
- Amazon S3
- IAM
- AWS CLI

---

# Learning Objectives

This project helped me improve my skills in:

- DevOps fundamentals
- CI/CD automation
- GitHub Actions workflows
- AWS infrastructure automation
- Infrastructure as Code (IaC)
- Cloud deployment pipelines
- AWS Lambda deployment
- CloudFormation validation

---

# Future Improvements

- Add Terraform support
- Add Docker integration
- Implement multi-environment deployment
- Add monitoring with CloudWatch
- Add automated testing stage
- Add rollback strategy

---

# Author

## Alperen Bulut

- AWS Certified Solutions Architect – Associate
- AWS Certified Cloud Practitioner
- AWS Certified AI Practitioner

GitHub: https://github.com/Alperenblt

LinkedIn:
https://www.linkedin.com/in/alperen-bulut-/
