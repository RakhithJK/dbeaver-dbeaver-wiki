* [Import from email](#import-from-email)
* [Import from the personal account](#import-from-the-personal-account)
* [Insert the License key into the License Manager](#insert-the-license-key-into-the-license-manager)
* [Import of Subscription license](#import-of-subscription-license)
* [Import of License extension](#license-extension)
* [License Manager](#license-manager)

To start using commercial versions of DBeaver you can

* request a [Trial license](https://dbeaver.com/trial/) for 2 weeks;
* request an [Academic license](https://dbeaver.com/academic-license/) if you are a student or a teacher;
* [buy](https://dbeaver.com/buy/) a Subscription license, Standard DBeaver license or DBeaver license extension.

After purchasing the DBeaver license or getting the Trial/Academic license, you will receive a License text by email. 
It will also be available in your personal account on our [site](https://dbeaver.com/).
This License text will contain your License ID e. g. DB-841MRZHY-ZH54, the start date and license owner’s name and company name. It is very important to import your License correctly.

### Import from email

You can just copy-paste the License Key to import the license into the License Manager. Please note that you need to copy-paste the full license text (not just the license ID). The license text starts with “–” and ends with “==” characters.

![](images/license/mail.png)

Sometimes an email client can corrupt the formatting of the License Key that can cause an error.

![](images/license/error.png)

Therefore, you need to import your License Key from your personal account on our site https://dbeaver.com/.

### Import from the personal account

Firstly, you need to [Sign in](https://dbeaver.com/signin/).

Secondly, you should open the **Licenses** tab, where you can find all your licenses. 

![](images/license/tab.png)




To open License details and copy the license key text click the license ID link. Here you can find your license status, type, maintenance period, and end support date.




![](images/license/details.png)

At the bottom of the page you can find the License Key required to start using DBeaver.
There are two options how to copy your License Key from the personal account:

1)Press the **COPY TO CLIPBOARD** button, then press OK. The license text will be copied to the clipboard.

![](images/license/lic-copy.png)

2)Press the **DOWNLOAD LICENSE** button, then press OK. 

.txt file with your License Key will be downloaded to your download folder. The file name is License ID, e. g. DB-841MRZHY-ZH54.

![](images/license/lic-download.png)

Then you need to insert the copied License Key to License Manager in DBeaver.

### Insert the License key into the License Manager

To start using commercial versions of DBeaver with your License Key you need to open License Manager in DBeaver:
Help -> DBeaver License Info

![](images/license/help-info.png)

The License information window can look different depending on whether you already have a valid license or not.

![](images/license/information.png)

Then you open the License Manager and press the Import button to paste your License Key.

![](images/license/lic-import.png)


If you copied the License Key to the clipboard, press the Paste button and then Import. 
If you downloaded a .txt file with the License Key, press the Load button and then select the file from Downloads. The License Key will be pasted automatically.
Then press the Import button and your license will be added to the License Manager. You have successfully imported your license.


![](images/license/manager.png)

You have successfully imported your license. Now you can close the License Manager and start using DBeaver.  

### Import of Subscription license

A subscription license requires internet access on the workstation for the first activation and each prolongation.

If you do not have an active internet connection or work behind a corporate firewall while importing the Subscription license, the following error can appear:

*Invalid subscription*

*Can`t find the subscription information for license ‘DB-841MRZHY-ZH54’.*

*Check your internet connection and/or firewall settings and restart application.*

In this case you need to check that DBeaver has internet access or you will need to configure your firewall.

### License extension

The standard DBeaver license is a perpetual license with a limited period of support (1 year or 2 years). 

After the end of the selected support period you can continue to use commercial versions of DBeaver without support and updates or buy a license extension or a new license.

If you buy the DBeaver license extension and DBeaver has internet access, the license in DBeaver will be updated automatically. Otherwise, you have to import the license key from your personal account once again.

### License Manager

License Manager provides you with the following information about your licenses:

* License ID e. g. DB-841MRZHY-ZH54;
* License type: Trial/Academic/Subscription/Standard;
* Version;
* License owner`s name and company name;
* License owner`s email;
* Start time is the date the license was received;
* End time is the date the license expires (standard perpetual licenses do not have this)
* Number of users: single user or multiuser for group licenses;
* Support period is the period you have access to the internal support system on the site and the possibility to download new product versions;
* State: valid or expired.

![](images/license/manager.png)
