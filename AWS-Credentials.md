DBeaver is integrated with AWS IAM authentication.  
Thus it provides the possibility to authenticate in AWS to access your cloud databases.  
To use IAM authentication in DBeaver, in connection configuration `AWS RDS IAM` should be selected as an authentication method:

![image](https://user-images.githubusercontent.com/20579256/205051128-71dd099b-b6f8-4bad-85a4-19b122d9d624.png)

DBeaver AWS IAM has endless ways to authorize and authenticate users. DBeaver supports all basic ones.

You can select the credentials type by selecting the required credential in `Credentials` selector:

![image](https://user-images.githubusercontent.com/20579256/205051449-b5016103-c77e-45d2-9d2a-1910517c6310.png)

### Default credentials

When you use Default Credentials, AWS will then try to determine credentials by using the standard credential providers chain:

1. Java system properties
1. Environment variables
1. Web identity token from AWS STS
1. The shared credentials and config files
1. Amazon ECS container credentials
1. Amazon EC2 instance profile credentials
1. Amazon SSO credentials

Using default credentials is essentially the simplest way to integrate with various SSO providers and web identity providers, as they usually provide credentials through config files.

Please read the [AWS credentials documentation](https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/credentials.html) for a detailed explanation.  

To use Default credentials, enter the username in the `User` field and select the AWS region.

![image](https://user-images.githubusercontent.com/20579256/205052240-08e62849-717a-4d64-8f0f-68bdacdfced4.png)

### Access keys

It is the most straightforward way to authenticate. You only need to enter the IAM user access key and secret key. You can save them locally or (more securely) enter them every time you connect to a database.

![image](https://user-images.githubusercontent.com/20579256/205054374-a509af4a-2c20-4a36-87f7-69c3dc7547af.png)

As previously mentioned in the Default configuration, you should enter your username and select AWS region. Then, if you checked `Save credentials locally`, you need to fill in the `Access key` and `Secret key` fields. If `Save credentials locally` is not checked, the dialog asking to fill these fields will be prompted each time you connect to the database:

![image](https://user-images.githubusercontent.com/20579256/205054153-3a26d79a-f03f-48df-9488-47d0bafcd50a.png)

Official AWS instructions: [Managing access keys for IAM users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

### AWS Profiles

Similar to default credentials, but you can also choose which credentials profile you want to use.  

![image](https://user-images.githubusercontent.com/20579256/205054804-f88cc4a1-1602-4271-b0d7-3d3eb2217581.png)

First, select the available configured profile, information how it can configured can be found below, then as in previous examples fill in `User` field and select your AWS region.  

The official AWS instructions can be found at [credentials config files](https://docs.aws.amazon.com/credref/latest/refdocs/creds-config-files.html).

### [[Single Sign On|AWS-SSO]]

If your AWS account has a configured SSO portal, you can use a web-based SSO authorization.
SSO support can be enabled for Default and Profile-based AWS authorization types.  
You need to turn on the "Enable SSO" option.

![image](https://user-images.githubusercontent.com/20579256/205052749-6282508f-8a08-4280-bff3-4d32a3ae1bc5.png)

### AWS Secrets Manager
If you have a configured AWS Secret, you can use it to access your database. Secrets can be used for RDS databases and Redshift.
Instructions on how to create AWS Secret can be found [here](https://docs.aws.amazon.com/secretsmanager/latest/userguide/).
A Password field is required. 

To use this functionality tick `Use AWS Secrets Manager` and fill in the `Secret Name` field

![image](https://user-images.githubusercontent.com/20579256/205056415-8eef6bc5-9cb4-4914-b388-79598f814189.png)

#### Note
The secret needs to be in the same region as the database.