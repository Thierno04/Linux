* Tracking user accounts is very important, especially as a Linux server administrator.
* I'm exploring user and password expiration. This will include examples for lockout passwords, the chage command, and more!
```bash
sudo chage -E 2022-10-12 user
sudo chage -l user
sudo chage -m 7 user
sudo su - user
```

#### To recover the password
```bash
e
ro init=/bin/bash or
rw init=/bin/bash
passwd
reboot -f
```
```bash
ctrl + f2
passwd root
passwd user
ctrl + f1
```
