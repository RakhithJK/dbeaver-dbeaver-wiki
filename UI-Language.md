
### Changing interface language in Preferences

Go to Preferences->User Interface:

![](images/ug/UI-Language-Preferences.png)

Select your language in the drop-down list and click the "Apply and Close" button.  
If DBeaver is installed in a read-only directory, the automatic language change is not possible. In this case, try to edit the configuration file (see below).

### Changing interface language in configuration file

Locate the `dbeaver.ini` file. It is in the same directory where DBeaver is installed.

Open `dbeaver.ini` in a text editor and add the following lines before the line `-vmargs` 
```
-nl
XX
```

where XX is two-letter language code:

Language | Code
---|---
English | en
Chinese | zh
French | fr
Italian | it
Japanese | jp
German | de
Korean | ko
Portuguese (BR) | pt_BR
Russian | ru
Spanish | es
