# ECR cheat sheet

## aws ecr commands

```text
# get ecr registry credentials
aws ecr get-login-password --region <region>

# get ecr registry credentials and pipe to docker login command
aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.region.amazonaws.com

```

## References

* [awscli with ecr](https://docs.aws.amazon.com/AmazonECR/latest/userguide/getting-started-cli.html)
