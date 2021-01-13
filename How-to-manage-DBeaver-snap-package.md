## Install and Update

To download the dbeaver-ce snap package, run the following command:

```sudo snap install dbeaver-ce```

Or update it to the latest version:

```sudo snap refresh dbeaver-ce```

## Managing snap interfaces

In order to have access to the private and public keys located in ./ ssh, you need to manually connect the plugin:

```sudo snap connect dbeaver-ce:ssh-keys``` for access to private keys 

and 

```sudo snap connect dbeaver-ce:ssh-public-keys``` for access to public keys