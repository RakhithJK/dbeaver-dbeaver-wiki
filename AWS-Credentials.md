DBeaver is integrated with AWS IAM authentication.  
Thus it provides the possibility to authenticate in AWS in order to access your cloud databases.  

AWS IAM has endless ways to authorize and authenticate users. DBeaver supports all basic ones.

### Default credentials

When you use Default Credentials, AWS will then try to determine credentials by using the standard credential providers chain:

1. Java system properties
1. Environment variables
1. Web identity token from AWS STS
1. The shared credentials and config files
1. Amazon ECS container credentials
1. Amazon EC2 instance profile credentials
1. Amazon SSO credentials

Using default credentials is essentially the simplest way to integrate with various SSO providers and web identity providers as they usually provide credentials through config files.

Please read the [AWS credentials documentation](https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/credentials.html) for a detailed explanation.  

### Access keys

It is the most simple way to authenticate. You only need to enter the IAM user access key and secret key. You can save them locally or (more securely) enter them every time you connect to a database.

Official AWS instructions: [Managing access keys for IAM users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

### AWS Profiles

Similar to default credentials but you can also choose which credentials profile you want to use.  
The official AWS instructions can be found at [crednetials config files](https://docs.aws.amazon.com/credref/latest/refdocs/creds-config-files.html).

### [[Single Sign On|AWS-SSO]]

If your AWS account has configured SSO portal then you can use a web-based SSO authorization.
SSO support can be enabled for Default and Profile-based AWS authoriation types.  
You need to turn on the "Enable SSO" option.  
