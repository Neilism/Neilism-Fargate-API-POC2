
# Terraform Fargate POC

A proof of concept for an api deployed on AWS ECS Fargate with a ci/cd pipeline integrated with a github repo.

Review Terraform_Plan.log for details of aws components being provisioned



## Prerequisites

    1. Git & Terraform clients
    2. AWS toolkits - AWS CLI, AWS-IAM-Authenticator



## Usage

	1. Clone the Fargate Demo app Api Project : https://github.com/Neilism/Fargate-Terraform-POC
	2. Clone this Fargate API POC Project
	3. Update Fargate-API-POC/terraform.tfvars with appropriate values
	4. Run Terraform Plan and Apply
	5. Verify Aws resources created in aws console
	6. Configure dns to point to appropriate name_servers
	7. Send get request to route 53 domain name/alb domain name
	8. Verify app version running in response
	9. Change app version in Fargate Demo App  (server.js) and commit changes
	10. Verify CodePipeline kicked off processes in aws console
	11. Send get request to route 53 domain name/alb domain name
    13. Verify new app version running in response

    
## Roadmap

    1. Multi Region and AZ active-active configuration
    2. Custom API throtlling using API Gateway
    3. Canary / Blue-Green Deployment Setup
    4. Dead-letter queue mechanism to retain, investigate, and retry failed transactions
    5. Perform load test using burst strategy with random intervals of idleness
    6. To reduce latency for end users, you can use Global Accelerator or CloudFront
    7. Using AWS WAF to protect against attacks from common web exploits
    8. Configuring mutual TLS authentication
    9. Use CloudWatch Logs or Amazon Kinesis Data Firehose to log requests




