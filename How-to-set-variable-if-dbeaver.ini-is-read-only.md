If you need to set some variable and `dbeaver.ini` have read-only permissions (this can happen, for example, in a flatpack or snapcraft), you can use the `config.ini` 

## config.ini path: 

### For linux:

`~/.eclipse/org.jkiss.dbeaver.product_{version}/configuration/config.ini`

Your product version you can find when open DBeaver `Help -> About`

## Example

For example, you can set system property with your custom path to point to the keystore in **config.ini**

`-Djavax.net.ssl.truststore=<path>`