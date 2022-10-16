# FTP
### File Transfer Protocol

The File Transfer Protocol is a communication protocol used for the transfer of computer files between a client and server on a computer network.

Uses TCP/IP

FTP also used to upload/download files from websites and servers.
```bash
                      FTP
CLIENT (ftp) ---------------------->  SERVER (vsftpd)
Server1                               Server1
```
#### Remote Servers FTP Setup:

* Need root access
* Install vsftpd service (if not already)
* yum install vsftpd

#### Config:
```bash
/etc/vsftpd/vsftpd.conf
```
```bash
Remote SERVER                                 Client SERVER 
rpm -qa | grep vsftpd                 =       echo "This is test file from client linux" > myfile.txt
su -                                  =       ftp 192.168.0.0 
yum install vsftpd -y                 =       put myfile.txt
cd /etc/vsftpd/                       =       mput file1 file2 (multiple files)
ls                                    =
cp vsftpd.conf vsftpd.conf.org        =
ls -ltr
vi vsftpd.conf
systemctl start vsftpd.service
systemctl status vsftpd.service
systemctl stop firewalld.service
ifconfig
```

#### Remote Server FTP Setup:

Config Changes
```bash
/etc/vsftpd/vsftpd.conf
```
```bash
* anonymous_enable=NO
Uncomment
* ascii_upload_enable=YES
* ascii_download_enable=YES
May add
* use_localtime=YES
```
```bash
* Start and enable vsftpd service
*  systemctl start/enable/ vsftpd.service
* Stop firewalld or allow FTP to firewalld
```bash
We will temporarily stop firewalld
```bash
  systemctl stop firewalld
```
#### Client Server FTP Setup:

* Need root access
* Install ftp service (if not already)
* yum install ftp

#### How to transfer file ?
```bash
* ftp 192.168.0.0 (ip of remote server)
* Enter username/password
* put <file_name>
```
