### Overview 

Cloud Explorer provides a deep integration with classic cloud service providers such as Amazon, Google and Azure.  

__Note: Cloud Explorer is supported only in [[DBeaver Ultimate Edition|https://dbeaver.com/products/dbeaver-ultimate-edition/]].__
__Version 21.0 support only AWS (Amazon Cloud Services) cloud.__

It allows users to configure cloud access once and then easily browse, connect and manager all cloud databases with just a few clicks.  
There is no need to configure each database connection manually, all database endpoint information reads directly from the cloud provider.
Authentication is managed in a centralized mode - you use your cloud account to get access to the cloud databases.  

### Cloud configuration

Before you begin to work with cloud explorer you need to configure your cloud provider access.
Configuration includes access credentials, availability zones which will be used to search databases and some other cloud-specific settings.
Cloud configuration is different for each cloud service provider.

![](images/ug/cloud-explorer/main-toolbar.png)

### [[Configuring AWS cloud|AWS Cloud Explorer]]


### Explorer

One you configure the cloud configuration you can open the Cloud Explorer dialog and start adding database connections.
In the top drop-down of explorer dialog you can select the active cloud configuration or click "Edit" to change the cloud configuration.

In the center of the dialog you can see cloud databases in a hierarchical view. All databases are grouped by database/service type.
When you expand one of the top elements, DBeaver will start to search cloud databases in configured availability zones/regions.

![](images/ug/cloud-explorer/aws-cloud-databases.png)

If you have a large number of databases in your cloud, you can search or filter them using filter text above the cloud navigator.

You can drag-and-drop cloud databases directly to [[database navigator view|Database Navigator]] or [[projects view]].
You can also check any number of databases in the Cloud Explorer using the checkbox control on the left side of the Cloud Explorer tree, and then click on the "Add to Project" button in the bottom right corner.


### Database cloud information

You can always see your cloud database configuration in a special tab in the connection settings dialog.
This information depends on both cloud and database type.
You can also click on the external link to open your database configuration in the cloud provider web console.

![](images/ug/cloud-explorer/cloud-database-info-tab.png)
