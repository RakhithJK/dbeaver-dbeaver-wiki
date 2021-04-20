## External resources access

Sometimes DBeaver needs to access external internet resources for tasks such as:

- 3rd party JDBC drivers download
- Information about a new DBeaver version
- Connect to remote databases outside of your corporate network
- Subscription license activation (commercial version)
- License information update (commercial version)


If you are behind some corporate firewall which restricts access to external internet resources then it may become a real problem.  
Sometimes corporate firewalls allows access to external resources using a web browser but restricts this for all other applications.  

## How to configure a proxy for drivers download

You need to ask your network administrator about proxy parameters.  
Then go to Preferences->Connections->Drivers.  
![](images/ug/network/drivers-proxy.png)
You can enter a proxy host/port and (optionally) user/password here. It will be used for drivers download only.  
Drivers are usually downloaded from maven.org web site. You also may ask your network admin to add `maven.org` to the list of allowed external domains.

## How to configure network for license activation

You need to configure global proxy server.  
If you can't activate your subscription license then you first need to use a trial version to start DBeaver and configure a proxy.  

Go to Preferences->General->Network Connections:
![](images/ug/network/global-proxy.png)

Switch to Manual or Native proxy (native proxy settings will use an active web browser proxy configuration).  
Note: in order to activate/update a license DBeaver only needs to access the website `dbeaver.com`. You may ask your network administrator to add `dbeaver.com` to the white list.  

## How to configure a proxy for external databases access

You can configure proxy settings for an individual connection.  
You may set the proxy settings manually or use active OS/web browser settings:

![](images/ug/network/connection-proxy.png)

