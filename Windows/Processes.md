# Processes owning a ports
https://stackoverflow.com/questions/48198/how-do-i-find-out-which-process-is-listening-on-a-tcp-or-udp-port-on-windows

```
netstat -aon > C:\temp\netstatOUT.txt
```

Checking the contents of the output file:
```
TCP    127.0.0.1:5005         0.0.0.0:0              LISTENING       15240
```

You can then kill the process with the id in task manager.

# Force kill a process
__Admin power shell__
```
taskkill /pid 2764 /f
```