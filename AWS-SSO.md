# Using AWS Single Sign On in DBeaver

[AWS Single Sign-On](https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html) is a cloud-based single sign-on (SSO) service that makes it easy to centrally manage SSO access to AWS resources.  
You don't need to specify any user credentials explicitly in DBeaver connections configuration. All authorization is performed in web browser in 3rd party SSO provider, e.g. Google workspace, Microsoft AD portal, Facebook, etc.

## AWS CLI

You need to install AWS CLI (Command Line Interface) utilities to enable SSO authorization.  
[AWS CLI installation](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

AWS CLI version 2.2 is recommended.

## AWS SSO configuration

If you are in a corporate environment where all AWS configurations are provided by system administrators then you don't need to configure SSO parameters.
Otherwise you need to open command shell (<kbd>win+R</kbd>), enter `aws configure sso`, press enter and provide required parameters. 
Read [configuration instructions](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-sso.html) for the details.  

Restart DBeaver after AWS CLI SSO configuration will finish.  

## Connection configuration

In DBeaver database connection dialog you need to:
- Set Authentication to `AWS IAM`.
- Set Credentials to `AWS Profile`.
- Choose profile which was configured with AWS SSO (see previous chapter).
- Click on  `Enable SSO` check.

Now you can connect. DBeaver will open web browser with SSO authorization.  