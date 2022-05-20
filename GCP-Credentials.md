DBeaver is integrated with Goofle Cloud IAM authentication.  
Thus it provides the possibility to authenticate in GCP to access your cloud databases. 

### Default credentials

When you use Default Credentials, Google Cloud will then try to determine credentials by using the standard credential providers chain:

1. Environment variables (GOOGLE_APPLICATION_CREDENTIALS)
1. Identity token from GCP CLI
1. The shared user or service credentials and config files (usually application_default_credentials.json in AppData)
1. Google Compute Engine

Using default credentials is essentially the simplest way to integrate with various SSO providers and web identity providers as they usually provide credentials through config files.

Please read the [GCP authentication documentation](https://cloud.google.com/docs/authentication) for a detailed explanation.  

### Access key file

You can provide the path to your service credentials or user credentials file in the "Configuration" field.

You can read more about User and Service authentication [here](https://cloud.google.com/docs/authentication#principals)

### Web browser or [[Single Sign On|GCP-SSO]]

Google Cloud Shell will be used for authethication.
If your GCP account has a configured SSO portal, you can use a web-based SSO authorization.