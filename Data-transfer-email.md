**Note: The following feature is only available in [Enterprise](Enterprise-Edition) and [Ultimate](Ultimate-Edition) editions.**

DBeaver offers a way to send data exported via [Data Transfer](Data-transfer) by email.

### SMTP profile configuration

First, you will need to add an SMTP profile to sen`d the email from. Go to <kbd>Window</kbd> &rArr; <kbd>Preferences</kbd> &rArr; <kbd>General</kbd> &rArr; <kbd>Mail</kbd> and create a new profile.

Parameters <kbd>Host</kbd> and <kbd>Port</kbd> may depend on the mail service you use. If the service offers both SSL and TLS ports, use the latter one. Gmail, for example, uses host `smtp.gmail.com` and port `587`. An example of a configured profile:

![img_1.png](images/ug/data-transfer/mail-smtp-configuration.png)

Then you can use the <kbd>Test connection</kbd> button to verify that the host and credentials are valid.

See the [troubleshooting](#Authorization-troubleshooting) section for more information on resolving common authorization problems.

### Setting up data transfer
When at least one [profile](#SMTP-profile-configuration) is present, you can actually set up email sending. Create a regular export task, go to the <kbd>Output</kbd> page and make sure the <kbd>Send results by E-Mail</kbd> option is enabled. By pressing the <kbd>Configure</kbd> label near it, you can specify several recipients and the subject for your mail:

![](images/ug/data-transfer/mail-configuration.png)

That's it. After the task is completed, the specified recipients will receive an email containing the exported file in a specified format during the data transfer.

### Authorization troubleshooting

You may face various problems while setting up a new SMTP profile.

Several common errors when using Gmail and solutions for them are described below:
- `535-5.7.8 Username and Password not accepted`. Check that the username and password are correct. If you are certain that you have entered valid credentials, then try allowing less secure apps.<br>Read more at https://support.google.com/accounts/answer/6010255
- `534-5.7.9 Application-specific password required`. You have two-factor authorization enabled. You will need to generate a special password for DBeaver to use.<br>Read more at https://support.google.com/accounts/answer/185833

There were also several cases when antivirus' would block DBeaver from sending an email.