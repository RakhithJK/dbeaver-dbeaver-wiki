Sometimes the database cannot be accessed directly, in such cases you can use the SSH tunnel. The SSH or Secure Shell is a network communication protocol that allows two computers to communicate and encrypts the shared data. 

DBeaver supports the following SSH authentication methods:
 - Username/password
 - Public key authentication
 - Agent authentication

Available agent authentication implementations:
 - [pageant](https://www.digitalocean.com/community/tutorials/how-to-use-pageant-to-streamline-ssh-key-authentication-with-putty) _(Windows only)_
 - [ssh-agent](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

Note that you have to run the agent first before connecting to the database in DBeaver.

## Configuring SSH

SSH can either be configured individually for each connection in <kbd>Connection settings</kbd> &rArr; <kbd>SSH</kbd><sup>1</sup> or as a [network profile](Network-Profiles) which can be selected from the drop-down menu<sup>2</sup> on the same page mentioned earlier:

![](images/ug/network/ssh/ssh-configuration.png)

In order to use SSH, you have to enable it first. After that, configure it for your needs, then click on <kbd>Test tunnel configuration</kbd> to test whether all parameters are valid or not.

It is often required to set the hostname to `localhost` in <kbd>Connection settings</kbd> &rArr; <kbd>Main</kbd>. SSH establishes a connection between two machines, authenticating each side to the other, and passing commands and output back and forth. After connecting to remote machine, all commands you execute are executed on that remote machine, so by having the host set to `localhost` you are opening a connection to the database on this remote machine, not on your local machine, and just redirect I/O to the latter. 

## Configuring Gateway Host

Gateway host, sometimes known as jump host, is used in situations when you cannot access a particular machine directly from your local machine, but it is possible to use a gateway server.

Just like SSH configuration, you have to enable it first. Gateway has the same configuration as for regular SSH tunnel:

![](images/ug/network/ssh/jump-server-configuration.png)

### Practical use
Imagine you have the following situation: your database is located on remote machine with IP address `100.100.100.100` and which is accessible through SSH. You cannot access this IP directly from your machine because of your network settings or firewall, but you can access other machines with the IP address `200.200.200.200` through SSH and which **is able** to access the desired remote machine.
You will need to specify `100.100.100.100` as a host in regular SSH configuration and `200.200.200.200` as a host in a gateway configuration to achieve such a "connection order": `localhost` &rarr; `200.200.200.200` &rarr; `100.100.100.100`.

### Availability note
Jump servers are only available with Jsch implementation. See information [below](SSH-Configuration#advanced-options).

## Advanced options

![](images/ug/network/ssh/advanced-options.png)

1. Optional port forwarding configuration, see information at [below](SSH-Configuration#port-forwarding).
1. Keep-alive interval. Can be used to "ping" a remote machine to make sure that the SSH connection is still alive.
1. Connection timeout. If the destination SSH machine is quite slow and the connection takes ages to complete, you can adjust the value of this parameter.

### Port Forwarding

Port forwarding is used to expose some socket sitting on a remote port to your local port, allowing you to communicate with it. After the SSH connection to the remote machine is established, you now need to connect to the database on that machine. Now you need to pass the port on which the database is listening to from that remote machine to your local machine. This is when port forwarding becomes handy.

By default, it randomly chooses the local port and forwards it to the destination port set in <kbd>Connection settings</kbd> &rArr; <kbd>Main</kbd>

It is not usually required to change this configuration, but it can be useful e.g. when you want to use a particular local port.