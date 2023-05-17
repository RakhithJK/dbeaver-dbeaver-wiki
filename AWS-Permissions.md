### AWS managed policies you need to assign to user for make CloudExplorer works.

Service | Read Policy | Write Policy
---|---|---
Login | - | 
Cloud Explorer | - | 
S3 | [AmazonS3ReadOnlyAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonS3ReadOnlyAccess) | [AmazonS3FullAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonS3FullAccess)
Redshift | [AmazonRedshiftReadOnlyAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonRedshiftReadOnlyAccess) | [AmazonRedshiftFullAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonRedshiftFullAccess)
RDS | [AmazonRDSReadOnlyAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonRDSReadOnlyAccess) | [AmazonRDSFullAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonRDSFullAccess)
DynamoDB | [AmazonDynamoDBReadOnlyAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonDynamoDBReadOnlyAccess)| [AmazonDynamoDBFullAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonDynamoDBFullAccess)
DocumentDB | [AmazonDocDBReadOnlyAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonDocDBReadOnlyAccess) | [AmazonDocDBFullAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonDocDBFullAccess) 
Keyspaces | [AmazonKeyspacesReadOnlyAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonKeyspacesReadOnlyAccess) | [AmazonKeyspacesFullAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonKeyspacesFullAccess)
Athena | | [AmazonAthenaFullAccess](https://us-east-1.console.aws.amazon.com/iamv2/home?region=eu-central-1#/policies/details/arn%3Aaws%3Aiam%3A%3Aaws%3Apolicy%2FAmazonAthenaFullAccess)
Redis | | 
