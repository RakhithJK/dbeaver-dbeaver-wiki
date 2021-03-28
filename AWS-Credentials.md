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

Essentially using default credentials it is the simplest way to integrate with various SSO providers and web identity providers as they usually provide credentials thru config files.

Please read [AWS credentials documentation](https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/credentials.html) for detailed explanation.  

### Access keys

It is the most simple way to authenticate. You jsut enter IAM user access key and secret key. You can save them locally or (more secure) enter them every time you connect to a database.

Official AWS instructions: [Managing access keys for IAM users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

### AWS Profiles

Similar to default credentials but you also can choose what credentials profile you want to use.  
Official AWS instruction on [crednetials config files](https://docs.aws.amazon.com/credref/latest/refdocs/creds-config-files.html)
