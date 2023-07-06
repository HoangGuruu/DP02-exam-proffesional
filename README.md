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
### 17. CloudFormation - Termination Protection
- Edit Termination Protection to protect before delete
### 18. CloudFormation - EC2 User Data
- Create stack with 10cfn-init/1-ec2-user-data.yaml
- See logs in EC2
```
cat /var/log/cloud-init-output.log 
```
### 19. CloudFormation - CFN Init Overview
### 20. CloudFormation - CFN Init Scripts
### 21 CloudFormation - CFN Init Hands On
- Create stack with 10-cfn-init/2-cfn-init.yaml
	+ Create a S3 bucket with webappp (name.html simple app) and add name of bucket
	+ Have KeyName
	+ SSHLocation : 0.0.0.0/0
	
### 22. CloudFormation - Continue Rolling Back an Update
- Create stack with 14-deployment-options/continue-rollback.yaml
- Then check with delete Launch Configuration in ASG EC2 and create a new ones
- Then Update stack with another template 14-deployment-options/continue-rollback-failed.yaml
- Then check
### 23. CloudFormation - Custom Resources Overview
### 24. CloudFormation - Custom Resources with AWS Lambda
- Create stack with 16-advanced-resources/custom-resourceslambda-backed.yaml
- Add or upload file in S3 then check
- It will delete All in S3 and S3 if i choose delete Stack
### 25. ====== NOTE ======
### 26. CloudFormation - Service Role
- Add user
- Create policy with json 14/service-role/cloudformation-user-policy.json
- Then attach custom policy with user
- Create stack with 14/service-role/template.yaml
- Then can see Access denied
- Then edit policy - Add "ssm:GetPArameters"
- Delete stack
- Create role CloudFormation : FullEC2 , ssmONLYREAD
- Then again - In permissions add role ARN
- Then check 
### 27. CloudFormation - SSM Parameters
### 28. CloudFormation - SSM Parameters Hands On
- Parameter Store
- name : /dev/ec2/instanceType
- data type :text
- value : t2.micro
- Then check Public parameters with /aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2
- Create stack with 3-parameters/1-ssm-parameters-hands-on.yaml
- Then add Parameters with ImageId and InstanceType
- Then check with change in Parameters t2.micro -> t2.nano then update with current stack
- AND CHECK
### 29. CloudFormation - Dynamic References
### 30. CloudFormation - Dynamic References Hands On
- 16-advanced-resources
- Create Parameter | /ec2/instanceType - t2.micro | /iam/userPassword - Choose SecureString - Value: supersecretpassword
- Go to Secrets Manager - Store a new secret
- Choose other type of secrets
	+ username : administrator
	+ password : MySecretPassword124$10
- Change value of /iam/userPassword - Value: supersecretpassword$!121
- Create stack with 16-advanced-resources/dynamic-references.yaml - KeyName
- Then Check
### 31. CloudFormation - StackSets
### 32. CloudFormation - StackSets Hands On
- Create stack with 13-stacksets/AWSCloudFormationStackSetAdministrationRole.yml
- Create stack with 13-stacksets/AWSCloudFormationStackSetExecutionRole.yml
	+ Pass AcountId in Parameters { in console }
- Create stackset with 13-stacksets/enable-aws-config.yaml
	+ Deploy stacksets in this account
	+ Sign in with number ID account
	+ Add region
	+ Deployment options
- Then check , we will see stacksets in 2 region 
### 33. CloudFormation - StackSets Updates Hands On
- Add stack in stackset
	+ Account Id : 
	+ Region : 
### 34. CloudFormation - StackSets Drift
- Action - detection drift
### 35. CloudFormation - StackSets Delete Hands On
- Delete , if retain - can save invidial , and delete all 
### 36. Service Catalog - Overview
### 37. Service Catalog - Extras
### 38. Elastic Beanstalk - Overview
### 39. Elastic Beanstalk - Hands On
- Create a first application
- Name : MyApplication-dev
- Environment: MyApplication-dev
- Platform : Node.js
- Application code : sample application
- Config service access 
	+ Create IAM role :  
	+ EC2 to AWSElasticBeanstalkWebTier
	+ AWSElasticBeanstalkWorkerTier
	+ AWSElasticBeanstalkMulticontainerDocker
	
	+ Then choose this role in EC2 instance profile
	+ And service role : Create and use new service role
- Then check CloudFormation
- Check EC2
- Check Elastic Beanstalk

### 40. Elastic Beanstalk - High Availability Environment
- Create Application
- Name
- Environment : MyApplication-Prod
- Platform : Node.js
- Sample application
- Preset : Choose High availability
- Choose sevice exits - and ...
- Because choosing High availability so 
	+ VPC
	+ Public IP address , choose all , not actived
	+ Enable database if use
- NEXT
- Capacity : load balanced 1-4
- choose t3.micro only 
- NEXT
- 
- You can choose skip overview and create new environment
- Check output
### 41. Elastic Beanstalk - Deployment Modes
### 42. Elastic Beanstalk - Deployment Modes Hands On
- Check in Rolling updates and  deployments
- Test deploy with code of sample application
- { Should do agian and check }
### 43. Elastic Beanstalk - Extras

### 44. Serverless Application Model (SAM) - Overview
### 45. Serverless Application Model (SAM) with CodeDeploy
- [How to install sam and ... ](https://viblo.asia/p/xay-dung-ung-dung-tu-dong-convert-image-to-thumbnail-bang-sam-su-dung-trigger-khi-co-file-upload-vao-bucket-cua-s3-Qbq5QEWm5D8)
### 46. Cloud Development Kit (CDK) - Overview
- Use AWS CloudShell
```
# 1. install the CDK
sudo npm install -g aws-cdk-lib

# directory name must be cdk-app/ to go with the rest of the tutorial, changing it will cause an error
mkdir cdk-app
cd cdk-app/

# initialize the application
cdk init app --language javascript
# verify it works correctly
cdk ls

# 2. copy the content of cdk-app-stack.js into lib/cdk-app-stack.js
# In cdk/cdk-app-stack (1).js

# 3. setup the Lambda function
mkdir lambda && cd lambda
touch index.py

# 4. bootstrap the CDK application
cdk bootstrap

# 5. (optional) synthesize as a CloudFormation template
cdk synth


# 6. deploy the CDK stack
cdk deploy

# 7. empty the s3 bucket
# 8. destroy the stack
cdk destroy
```
### 44. Serverless Application Model (SAM) - Overview
### 45. Serverless Application Model (SAM) with CodeDeploy
- Check with terminal in VSC + Folder : sam-codedeploy 
```
# Step 1 - Download a sample application
sam init --runtime python3.9
# choose 1 - 1

# Step 2 - Build your application
cd sam-app
sam build

# Step 3 - Package your application
sam deploy --guided
```
- Go to lambda 
- Check in deployment , functions
- Check change in code and build , deploy again - then check deployment status
	+ traffic shift
### 46. Cloud Development Kit (CDK) - Overview
- Deploy your cloud infrastructure using a familiar language
- CDK vs SAM
### 47. Cloud Development Kit (CDK) - Hands On
![image](https://github.com/HoangGuruu/DevOps-Exam-Readiness-AWS-Certified-DevOps-Engineer-Professional/assets/111829092/9e03c568-1f6a-4374-82a4-c7b258706fb5)
- Use AWS CloudShell | Folder cdk | Follow the tutorial
```
# 1. install the CDK
sudo npm install -g aws-cdk-lib

# directory name must be cdk-app/ to go with the rest of the tutorial, changing it will cause an error
mkdir cdk-app
cd cdk-app/

# initialize the application
cdk init app --language javascript
# verify it works correctly
cdk ls

# 2. copy the content of cdk-app-stack.js into lib/cdk-app-stack.js
# content in folder

# 3. setup the Lambda function
mkdir lambda && cd lambda
touch index.py
# content in folder

# 4. bootstrap the CDK application
cdk bootstrap
# Get in CloudFormation in console to check


# 5. (optional) synthesize as a CloudFormation template
cdk synth


# 6. deploy the CDK stack
cdk deploy

#### Then check the results - add image in s3 bucket and check results of detection in dynamoDB

#### if want to finish
# 7. empty the s3 bucket
# 8. destroy the stack
cdk destroy
``` 
### 48. Step Functions - Overview
### 49. Step Functions - Hands On
- Go to Step Function in AWS Console
- Get start
- Do and check witj true / false

- Go to lambda 
- Create a lambda function / node.js
- Check with simple function , with code in folder 
```
exports.handler = (event,context,callback) => {
	callback(null, "Hello," + event.who + "!");
};
```
- Then check with test event
```
{
	"who": "John"
}
```
- This is for me to generate code with flow i want

### 50. AppConfig - Overview
### 51. Systems Manager (SSM) - Overview
### 52. Start EC2 Instances with SSM Agent - Hands On
- Launch 3 EC2 Amazon Linux 
	+ no key-pair
	+ no allow sg
	+ avanced : role : SSMManagedInstancdCore
- Check in Fleet Manager

### 53. AWS Tags & SSM Resource Groups
- Create Resource Groups in Console
- Choose follow required
### 54. SSM Documents & SSM Run Command
- Do simple hands-on to check results in AWS Systems Manager
- Create Command ... with code by YAML to install httpd
- Then run command / with resource manager : tag ...
- Enable CloudWatch
- Check the results

### 55. SSM Automations
- In AWS Systems Manager - Automation 
- Filter with : AWS-RestartEC2Instance
- Choose rate control
- Choose Targets
	+ InstanceId
	+ Resource Groups
	+ ....
- Execution


### 55. SSM Automations
- In AWS Systems Manager - Automation 
- Filter with : AWS-RestartEC2Instance
- Choose rate control
- Choose Targets
	+ InstanceId
	+ Resource Groups
	+ ....
- Execution

### 56. SSM Parameter Store
### 57. SSM Parameter Store - Hands On
- In AWS Systems Manager / Parameter Store
- Create parameter
	+ Name : /my-app/dev/db-url
	+ String
	+ Value : dev.database.stephanetheteacher:3306
- Create 2nd parameter
	+ Name : /my-app/dev/db-password
	+ SecureString
	+ My current account
	+ KMS Key ID: alias/tutorial
	+ Value :thisisthedevpassword
- Create 3rd parameter
	+ Name : /my-app/prod/db-url
	+ String
	+ Value : prod.database.stephanetheteacher:3306
- Create 4th parameter
	+ Name : /my-app/prod/db-password
	+ SecureString
	+ My current account
	+ KMS Key ID: alias/tutorial
	+ Value :thisistheprodpassword
- Check in CLI AWS
```
aws ssm get-parameters --names /my-app/dev/db-url /my-app/dev/db-password

aws ssm get-parameters --names /my-app/dev/db-url /my-app/dev/db-password

aws ssm get-parameters-by-path help

aws ssm get-parameters-by-path --path /my-app/dev/

aws ssm get-parameters-by-path --path /my-app/ --recursive

aws ssm get-parameters-by-path --path /my-app/ --recursive --with-decryption

```

### 58. SSM Patch Manager and Maintenance Windows
### 59.  SSM Patch Manager and Maintenance Windows - Hands On
- In Patch Manager / AWS Systems Manager
- Patch now
	+ Scan and install
	+ Reboot if needed
	+ Patch all instances
- Create Maintenance schedule



### 60. SSM Session Manager
### 61. SSM Session Manager - Hands On
- Start Session / with a EC2 instance
- Adjust parameter : example : hour to use 1 session ,....

### 62. SSM Cleanup
### 63. SSM Default Host Management Configuration (DHMC)
### 64. SSM Default Host Management Configuration (DHMC) - Hands On
- Fleet Manager
- Configure DHMC
- In EC2 launch instance
	+ amazon linux 2023
	+ Advanced : Metadata : enable | V2 only
- Check Default Host Management Configuration
- Manually installing SSM Agent on EC2 instances for Linux
- Install lastest version
- Refresh fleet manager to see instances

### 65. SSM Hybrid Environments
### 66. SSM Hybrid Environments - Hands On
- Create activation in SSM Hybrid
- Instance limit : 1 
- Get in Instances Ubuntu ( create )
```
#!/bin/bash
# if you need to install the SSM Agent manually:
sudo yum install -y https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/latest/linux_amd64/amazon-ssm-agent.rpm

# check status ubuntu
sudo systemctl status snap.amazon-ssm-agent.amazon-ssm-agent.service
sudo snap stop amazon-ssm-agent
# edit the code, id and region in the command below
sudo /snap/amazon-ssm-agent/current/amazon-ssm-agent -register -code "activation-code" -id "activation-id" -region "region" 
sudo snap start amazon-ssm-agent
```
- Check instance manager in Fleet Manager

### 67. SSM with IoT Greengrass
### 68. SSM Automations - Use Cases
### 69. SSM Compliance
### 70. SSM OpsCenter
### 71. SSM Session Manager with VPC Endpoints
### 72. AWS OpsWorks - Getting Started Part 1
- Get in OpsWorks in Console
- Add your first stack
- Sample stack
- Explore
- Stack settings
- Check all parameter of application
- Edit with instances

### 73. AWS OpsWorks - Getting Started Part 2
- Edit time-based / instances
- Add a time-based instances
	+ In another subnet
	.... 
	+ Setting necessary, everything else
	+ Schedule for my instances
- Add a load-based instances
- Check in part deployment 
- Check in part monitoring
- Check in part Permission


### 74. AWS OpsWorks - Lifecycle Events
### 75. AWS OpsWorks - CloudWatch Events Integration
### 76. AWS OpsWorks - Summary & Cleanup

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
