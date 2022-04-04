When working in DBeaver under a corporate network, you can encounter an error similar to the following:

```Java
javax.net.ssl.SSLHandshakeException:PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target.
```

Here is how you can bypass it.

## Import certificates from your local Java

It's possible that your system administrator has installed a local Java and imported the required certificates to its keystore. We can use them to fix the issue.

### Step 1: locate your Java

#### Windows

Press Windows + R to open the Run window. Type `cmd` in the prompt and press OK. It will open the command prompt. In the command prompt, type the 
following and press Enter:

```cmd
where java
```

#### macOS 

Open the Terminal and execute the following command:

```zsh
/usr/libexec/java_home -V
```

#### Linux

Open a terminal and execute the following command:

```sh
readlink -e /usr/bin/java
```

### Step 2: Find the JRE in DBeaver's installation

It's pretty easy. Just find the path where you installed DBeaver and open the `jre` folder there.

### Step 3: Copy the cacerts

Open the folder with the Java you found in step 1. Locate the `cacerts` files under `/lib/security`, then copy-paste it into `<PATH_FROM_STEP_2>/lib/security`, replacing the old file. Restart DBeaver, and you are ready to go.