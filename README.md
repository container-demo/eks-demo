# Provision an EKS demo cluster with Terraform

Instructions: https://developer.hashicorp.com/terraform/tutorials/kubernetes/eks

### AWS

1. AWS account
2. AWS IAM user

### Install the AWS CLI

1. [Install](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
2. [Configure](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html)

```
% aws --version
aws-cli/2.11.5 Python/3.11.2 Darwin/22.3.0 exe/x86_64 prompt/off
```

```
% aws sts get-caller-identity
{
    "UserId": "YYA4ZRSAMPLE6IDAGV2YP",
    "Account": "378929636692",
    "Arn": "arn:aws:iam::378929636692:user/dockerbisson"
}
```

### Terraform Cloud

1. [Create account](https://app.terraform.io/signup/account)
2. Create an org
3. [Terraform variables with AWS credentials](https://developer.hashicorp.com/terraform/tutorials/cloud-get-started/cloud-create-variable-set)

### Terraform local

1. `brew install terraform`
2. `terraform init`
3. `terraform plan`
4. `terraform apply`

### kubectl config

Get `kubectl` config ([more details](https://repost.aws/knowledge-center/eks-cluster-connection)):

`aws eks --region example_region update-kubeconfig --name cluster_name`