# Linux System Monitoring Commands
* Linux df command
* Linux du command
* Linux free command
```bash
df command in linux
df command in linux with examples
disk usage linux
```

Linux System Monitoring Commands like df, df and free
using these commands we can monitor the Linux system and it's memory usage including physical memory and RAM available and usage.

We can use these commands to monitor the system and it's disk usage.
For example: if the available disk on the server is less than 20% we can generate an alert etc..
Also for the deployment of the application we must be pre aware of the available disk and RAM memory on the server.

```bash
df -h
df -h -BK
df -h -BG
du -h /home/user/folder/
du -ah /home/user/folder/
du -ahc /home/user/folder/
du -ahc -BK /home/user/folder/
```
```bash
free -h
free -h -s 3
free -h -c 4
```
