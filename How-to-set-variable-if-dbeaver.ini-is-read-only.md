If you need to set some variable and `dbeaver.ini` have read-only permissions (this can happen, for example, in a flatpack or snapcraft), you can use the `config.ini` 

## config.ini path: 

### For linux:

You can find correct path to your configuration directory with **config.ini** when open DBeaver `Help -> Installation Information -> Configuration` then _**type filter text**_ `osgi.configuration.area`

![image](https://user-images.githubusercontent.com/46003534/168042031-526fe1df-702c-4bb0-9e75-df5dece2af93.png)

***

If **config.ini** does not exist, you can create it in configuration directory `nano config.ini`

***

### For Windows:

You can find correct path to your configuration directory with **config.ini** when open DBeaver `Help -> Installation Information -> Configuration` then _**type filter text**_ `osgi.configuration.area`

Example output:

```
osgi.configuration.area=file:/C:/Users/user/AppData/Local/DBeaverUltimate/configuration/
```

## config.ini example

For example, you can set system property with your custom path to point to the keystore that you created

`-Djavax.net.ssl.truststore=/path/to/your/cert`

Or for example you can change language 

`osgi.nl=fr`