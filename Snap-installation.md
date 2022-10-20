## Installation 

For install _dbeaver-ce_ snap package with stable release (stable by default):

```snap install dbeaver-ce --stable```

## Connect interfaces:

You can find list of all _dbeaver-ce_ snap connections:

```snap connections dbeaver-ce```

And connect what you need. For example:

```snap connect dbeaver-ce:ssh-keys``` for access to private keys

Or you can do it in Ubuntu Software (dbeaver-ce - Permissions):

![image](https://user-images.githubusercontent.com/46003534/172124852-bee2766f-fcee-4deb-9cab-7d132dc02aae.png)


### Problems with dbeaver-ce snap package:

At the moment there is a well-known problem with opening the browser and gis maps via _dbeaver-ce_ snap package. Application crashes with an error:

`SWT WebKitGDBus: error creating DBus server Error binding to address (GUnixSocketAddress): Permission denied`
`SWT WebKit: error initializing DBus server, dBusServer == 0`


Snapcraft forum topic: https://forum.snapcraft.io/t/classic-confinement-for-dbeaver-ce/27502

### Workaround

While the problem is being fixed, you can use the **workaround**:

Run _dbeaver-ce_ snap package from: ```/snap/dbeaver-ce/current/usr/share/dbeaver-ce/dbeaver``` 
