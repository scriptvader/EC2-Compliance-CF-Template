# EC2-Compliance-CF-Template
These templates help check coverage and compliance of SSM agents on your EC2 instances, and then using SSM inventory can also check the coverage of specified applications on your EC2 e.g EDR

## Description
The AWS CloudFormation Templates deploy a Lambda function triggered every 24 hours to run the compliance logic and update a conig rule with te complaince status of EC2 instances in the accoumt.

<img width="931" alt="image" src="https://github.com/scriptvader/EC2-Compliance-CF-Template/assets/28531392/2660e5ac-5b71-4703-8404-1e4254247231">

The "Template" folder contains two yaml files, one to check SSM coverage and the other for Applications.

The Applications template allows you to specify one or more applications to check compliance for, and also to specify the logic:
* OR - for more that one application, instance will return compliant if at least one application is present
* AND - for more that one application , instance will return compliant if all applications are present

## AWS Resource Costs

As with most AWS services you will incur costs for usage. For this CloudFormation template the resources that incur costs are as follows

* Pricing:
  * <a href="https://aws.amazon.com/lambda/pricing/">Lambda pricing</a>
  * <a href="https://aws.amazon.com/config/pricing/">Config pricing</a>

## Template Output

In the CloudFormation Console you should be able to verify the following resources have been created in the case of each template:
* A Lambda Function
* A Config Rule
* A Config Permission to call Lambda
* An IAM role





