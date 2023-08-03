# AWS

Having your own data centers and servers requires resources and staffing.
Cloud computing reduces operation and lets you focus on important things, such as your applications and customers.

machines running in your AWS environments, such as Amazon EC2 instances or AWS Lambda functions.

AWS:
Console CLI CDK SDK
IAM CloudWatch S3 CloudFront EC2 Lambda DynamoDB RDS AuroraDB

AWS regions - where the AWS servers, datacenters are located
AWS region zones - servers at a area separated by long distance where the same data is replicated for safety

## Free tier

When your 12-month free usage term expires, or if your application use exceeds the tiers, you simply pay standard, pay-as-you-go service rates. Always Free – These free tier oﬀers do not expire and are available to all AWS customers.

## AWS services

### AWS IAM

AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. With IAM, you can centrally manage permissions that control which AWS resources users can access. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.

With AWS Identity and Access Management (IAM), you can specify who or what can access services and resources in AWS, centrally manage fine-grained permissions, and analyze access to refine permissions across AWS.

the 3 types of IAM principals?
Principals: Three types of Principals — root users, IAM users and Instance Principals. First IAM user is called the root user.

The five pillars of IAM: Lifecycle and governance; federation, single sign-on and multi-factor authentication; network access control; privileged account management; and key encryption.

### AWS CLI

AWS management console is a web application that allows its users to view, monitor, and manage resources offered by AWS. The Command Line Interface is another tool to manage AWS services. The core functionality provided by the Command Line Interface is the same as that of the console.

### AWS - CDK SDK

The AWS Cloud Development Kit (CDK) is a framework that allows you to provision Cloud infrastructure using code.

The AWS Software Development Kit (SDK) is a set of libraries that allow you to integrate your application with AWS Services.

### AWS S3

### AWS EC2

### AWS Lambda

Serverless

Deploy your code to Lambda
Make the code ready to trigger an event
The code only runs when triggered
Pay only when your code is running

### AWS CloudShell

AWS CloudShell is a browser-based, pre-authenticated shell that you can launch directly from the AWS Management Console. You can run AWS CLI commands against AWS services using your preferred shell, such as Bash, PowerShell, or Z shell. And, you can do this without needing to download or install command line tools.

Every shell environment that you run with CloudShell has the AWS Command Line Interface (CLI) (v2) installed and configured so you can run aws commands fresh out of the box. The environments also include the Python and Node runtimes, with many more to come in the future.
