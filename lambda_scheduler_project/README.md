# AWS Lambda Scheduler with Terraform

This project demonstrates how to create a scheduled AWS Lambda function using Terraform in 5 minutes.

## Structure

```
lambda-scheduler/
├── lambda/
│   ├── lambda_function.py
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
├── lambda.zip             # Generated zip file for Lambda
└── README.md
```

## Instructions

1. **Install Prerequisites**
   - Terraform: https://developer.hashicorp.com/terraform/downloads
   - AWS CLI: https://aws.amazon.com/cli/

2. **Zip Lambda Function**
   ```bash
   cd lambda
   zip ../lambda.zip lambda_function.py
   ```

3. **Deploy Using Terraform**
   ```bash
   cd terraform
   terraform init
   terraform apply -auto-approve
   ```

4. **Result**
   - A Lambda function triggered every 5 minutes.
   - Check CloudWatch Logs for output.

## License
MIT
