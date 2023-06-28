# AWS Certified DevOps Engineer Professional 2023 - DOP-C02 - Udemy

## I. ✅ Course Overview

## II. ✅ Code&Slides Download

## III. Domain 1: SDLC Automation

- ✅Introduction to CICD in AWS
- ✅CodeCommit - Overview
- ✅CodeCommit - Hands On Part 1
- ✅CodeCommit - Hands On Part 2
- ✅CodeCommit - Advanced
- ✅CodePipeline - Overview
- ✅CodePipeline - Hands On
- ✅CodePipeline - Extras
- ✅CodePipeline - CloudFormation Integration
- ✅CodePipeline - Advanced
- ✅CodeBuild - Overview
- ✅CodeBuild - Hands On Part 1
- ✅CodeBuild - Hands On Part 2
- ✅CodeBuild - Advanced
- ✅CodeDeploy - Overview
- ✅CodeDeploy - EC2 Deep Dive
- ✅CodeDeploy - ECS Deep Dive
- ✅CodeDeploy - Lambda Deep Dive
- ✅CodeDeploy - Rollbacks & Troubleshooting
- ✅CodeArtifact - Overview
- ✅CodeArtifact - Upstream Repositories & Domains
- ✅CodeArtifact - Hands On
- ✅CodeGuru - Overview
- ✅CodeGuru - Extras
- ✅EC2 Image Builder
- ✅EC2 Image Builder - Extras
- ✅AWS Amplify
- ✅AWS Amplify - Extras

## IV. Domain 2: Configuration Management and Infrastructure as Code
## Hands-on
### 1. CloudFormation - Overview
### 2. Create Stack Hands-on

- In cloudFormation / Stacks
- Template is ready
- Upload a template

```
---
Resources:
	MyInstance:
		Type: AWS::EC2::Instance
		Properties:
		AvailabilityZone: us-east-1a
		ImageId: ami-a4c7edb2
		InstanceType: t2.micro
```
### 3. Update & Delete Stack

```
# template 2nd

1-ec2-with-sg-eip

```
### 4. YAML Crash Course

### 5. CloudFormation - Resources
- Can find [resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html) in documentation

### 6. CloudFormation - Parameters
### 7. CloudFormation - Mappings
### 8. CloudFormation - Outputs
### 9. CloudFormation - Conditions
### 10. CloudFormation - Intrinsic Functions
### 11. CloudFormation - Rollbacks

- Create stack
- use 2-trigger....
- In stack failure options - choose in queried : Preserve .... OR ...
- Then check -- it's not ok

- And create again with 0 , then update with 2, then 2 failure , it roll on 0

### 12. CloudFormation - Drift
- Create stack with 3-drift-security-group.yaml
- Then change the results - edit the SecurityGroup and Check
- Stack actions / Detect drift / View drift

### 13. CloudFormation - Stack Policies

### 14. CloudFormation - Nested Stacks

- Create stack with 7-nestedstacks.yaml
- In this project - Choose SSHKey in Parameter
- In Capabilities : tick all 2
- Check - nestedstacks (it's can understand like URL: another stack in code)- outputs

### 15. CloudFormation - ChangeSets
- Create stack 0 
- Create change set in actions
- Upload stack 1 
- Then check changesets - before ... excute

### 16. CloudFormation - DeletionPolicy
- Create stack with 9
- Delete stack 
- Then check SG is retain and RDB have a snapshot appear and then deleted

  
- CloudFormation - Termination Protection
- CloudFormation - EC2 User Data
- CloudFormation - CFN Init Overview
- CloudFormation - CFN Init Scripts
- CloudFormation - CFN Init Hands On
- CloudFormation - Continue Rolling Back an Update
- CloudFormation - Custom Resources Overview
- CloudFormation - Custom Resources with AWS Lambda
====== NOTE ======
- CloudFormation - Service Role
- CloudFormation - SSM Parameters
- CloudFormation - SSM Parameters Hands On
- CloudFormation - Dynamic References
- CloudFormation - Dynamic References Hands On
- CloudFormation - StackSets
- CloudFormation - StackSets Hands On
- CloudFormation - StackSets Updates Hands On
- CloudFormation - StackSets Drift
- CloudFormation - StackSets Delete Hands On
- Service Catalog - Overview
- Service Catalog - Extras
- Elastic Beanstalk - Overview
- Elastic Beanstalk - Hands On
- Elastic Beanstalk - High Availability Environment
- Elastic Beanstalk - Deployment Modes
- Elastic Beanstalk - Deployment Modes Hands On
- Elastic Beanstalk - Extras
- Serverless Application Model (SAM) - Overview
- Serverless Application Model (SAM) with CodeDeploy
- Cloud Development Kit (CDK) - Overview
- Cloud Development Kit (CDK) - Hands On
- Step Functions - Overview
- Step Functions - Hands On
- AppConfig - Overview
- Systems Manager (SSM) - Overview
- Start EC2 Instances with SSM Agent - Hands On
- AWS Tags & SSM Resource Groups
- SSM Documents & SSM Run Command
- SSM Automations
- SSM Parameter Store
- SSM Parameter Store - Hands On
- SSM Patch Manager and Maintenance Windows
- SSM Patch Manager and Maintenance Windows - Hands On
- SSM Session Manager
- SSM Session Manager - Hands On
- SSM Cleanup
- SSM Default Host Management Configuration (DHMC)
- SSM Default Host Management Configuration (DHMC) - Hands On
- SSM Hybrid Environments
- SSM Hybrid Environments - Hands On
- SSM with IoT Greengrass
- SSM Automations - Use Cases
- SSM Compliance
- SSM OpsCenter
- SSM Session Manager with VPC Endpoints
- AWS OpsWorks - Getting Started Part 1
- AWS OpsWorks - Getting Started Part 2
- AWS OpsWorks - Lifecycle Events
- AWS OpsWorks - CloudWatch Events Integration
- AWS OpsWorks - Summary & Cleanup

## VI. Domain 3: Resilient Cloud Solutions

## VII. Domain 4: Monitoring and Logging

## VIII. Domain 5: Incident and Event Response

## IX. Domain 6: Security and Compliance

## X. Other Services

## XI. Domain 1 - OLD: SDLC Automation

## XII. Domain 2 - OLD: Configuration Management and Infrastructure as Code

## XIII. Domain 3 - OLD: Monitoring and Logging

## XIV. Domain 4 - OLD: Policies and Standards Automation

## XV. Domain 5 - OLD: Incident and Event Response

## XVI. Domain 6 - OLD: High Availability, Fault Tolerance, and Disaster Recovery

## XVII. Other Services
