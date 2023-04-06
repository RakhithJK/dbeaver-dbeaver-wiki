Sometimes (due to some bug) DBeaver UI hangs, freezes or works incorrectly. It is usually impossible to find the reason of such a problem without a thread dump. A thread dump is the information about the internal execution state of the Java program. To get thread dump:

#### Mac and Linux
Run the following on your terminal:
```
jstack $(ps aux | grep java | grep dbeaver | awk '{print $2}') > thread-dump.txt
```

#### Windows
Open the task manager (<kbd>CTRL+SHIFT+ESC</kbd>), find DBeaver in the process list, and copy its process ID value. In Windows 8+ you need to switch to the "Details" tab.

Open the command prompt (<kbd>Win+R</kbd> and type `cmd`, then press <kbd>ENTER</kbd>), run the following command:

```bash
jstack PID > thread-dump.txt
```

The produced file will be located in the user's home folder, e.g. `C:\Users\Username`.

Now you can attach thread-dump.txt to the GitHub issue.