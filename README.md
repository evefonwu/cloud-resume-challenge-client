# Cloud Resume Challenge

This is the **Client app** of the **_Cloud Resume Challenge_**

UPDATE: Updated previously completed Cloud Resume Challenge to use GitHub Action Secrets instead for values such as the API URL and GitHub Action OIDC IAM Role ARN.

- [API repo](https://github.com/cloud-resume-challenge-api)
- [Client repo](https://github.com/cloud-resume-challenge-client)

## Project Overview

The challenge is to build a full stack serverless application in the Cloud.

I built this project leveraging the following technologies and AWS services:

- AWS CloudFormation for infrastructure provisioning and management
- S3 bucket for site content storage, has bucket policy for data protection
- CloudFront Distribution for global fast content delivery that is cheaper than with S3 alone
- HTML for static content and dynamic view counter
- JavaScript to invokes API endpoint to effect change in the database
- API triggers Lambda function execution
- Lambda function updates DynamoDB view count value, returns updated count
- Lambda function returns CORS headers, controlling cross-origin resource access
- Automated CI/CD workflow with GitHub Actions, integrating code changes and deploying to AWS account
- Python smoke test from API to DynamoDB
- Cypress E2E Test of live site
- CloudWatch Alarms to monitor for API 4xx Errors and alert with email notifications

- **Security**

  - IAM resource access control
  - Certificate Manager (SSL) encrypted data in-transit
  - S3 bucket policy
  - CloudFront Origin Access Control for data protection
  - Federate GitHub OIDC provider with AWS for an IAM role temporary credentials for access

- **Availability, Reliability**

  - Managed services are build upon the availability and reliability of the AWS Global Infrastructure

- **Performance**

  - CloudFront Distribution provides caching and fast content delivery
  - AWS Lambda scales automatically to meet demands

- **Cost Optimization**

  - Serverless provisioning costs much less than a server-based solution

- **DevOps**

  - AWS CloudFormation infrastructure provisioning
  - Automated CI/CD workflow with GitHub Actions
  - CloudWatch Alarms to monitoring and alerting

- **_Project Article_**: ["Preparing for a Cloud Engineering Role"](https://dev.to/evefonwu/preparing-for-a-cloud-engineering-role-bof)
- The Challenge: [Cloud Resume Challenge - AWS](https://cloudresumechallenge.dev/docs/the-challenge/aws/)
