If you need to set some variable and `dbeaver.ini` have read-only permissions (this can happen, for example, in Flatpak or Snap), you can use the `config.ini`.

## config.ini path: 

### For Linux:

You can find correct path to your configuration directory with **config.ini** when open DBeaver `Help -> Installation Information -> Configuration` then _**type filter text**_ `org.osgi.framework.storage`

![image](https://user-images.githubusercontent.com/46003534/168237839-9c8a79ba-e49e-4639-9fe7-d898b3c3c324.png)

***

If **config.ini** does not exist, you can create it in the configuration directory `nano config.ini`

***

### For Windows:

You can find correct path to your configuration directory with **config.ini** when open DBeaver `Help -> Installation Information -> Configuration` then _**type filter text**_ `org.osgi.framework.storage`

Example output:

```
org.osgi.framework.storage=file:/C:/Users/user/.eclipse/org.jkiss.dbeaver.product_22.0.5_1535670467_win32_win32_x86_64
```

***

If **config.ini** does not exist, you can create it in the configuration directory.

***

## config.ini example

For example, you can set system property with your custom path to point to the keystore you created.

`javax.net.ssl.trustStore=/path/to/your/cert`

Or, for example, you can change the language. 

`osgi.nl=fr`