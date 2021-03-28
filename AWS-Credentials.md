DBeaver is integrated with AWS IAM authentication.  
Thus it provides possibility to authenticate in AWS in order to access your cloud databases.  

AWS IAM has endless way to authorize and authenticate users, DBeaver support all basic ones.

### Default credentials

When you use default credentials type then AWS will try to determine credentials by using standard credential providers chain:

1. Java system properties
1. Environment variables
1. Web identity token from AWS STS
1. The shared credentials and config files
1. Amazon ECS container credentials
1. Amazon EC2 instance profile credentials

Please read [[AWS credentials documentation|https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/credentials.html]] for detailed explanation

### Access keys

### AWS Profiles