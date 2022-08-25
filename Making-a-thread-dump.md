Sometimes (due to some bug) DBeaver UI hangs, freezes or works incorrectly. It is usually impossible to find the reason of such a problem without a thread dump. A thread dump is the information about the internal execution state of the Java program. To get thread dump:

#### Mac and Linux
Run the following on your terminal:
```
jstack $(ps aux | grep java | grep dbeaver | awk '{print $2}') > thread-dump.txt
```
#### Windows
Just open the task manager (CTRL+Escape), find DBeaver in the process list and copy the process ID value. In Windows 8+ you need to switch to the "Details" tab.
Run
```
jstack <PID> > thread-dump.txt
```
in the Command Prompt.

Now you can attach thread-dump.txt to the GitHub issue.