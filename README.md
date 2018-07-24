# Install Oracle Database 18c with Ansible

These roles configure Oracle Database prerequisites and install it for CentOS 7.

## Requirements

- VirtualBox 5.2
- Vagrant 2
- Ansible 2.6
- Installation media file distributed by oracle.com

## Create VM and install the Oracle Database software

Place the installation media file into roles/oracle18c/files/ and run vagrant as follows;

```
$ cp /foo/bar/LINUX.X64_180000_db_home.zip roles/oracle18c/files/
$ vagrant up
$ vagrant provision
```

# To use

```
$ vagrant ssh
[vagrant@oracle18c ~]$ su - oracle
Password: (password is oracle)
[oracle@oracle18c ~]$ sqlplus / as sysdba

SQL*Plus: Release 18.0.0.0.0 - Production on 火 7月 24 12:10:03 2018
Version 18.3.0.0.0

Copyright (c) 1982, 2018, Oracle.  All rights reserved.



Oracle Database 18c Enterprise Edition Release 18.0.0.0.0 - Production
Version 18.3.0.0.0
に接続されました。
SQL> 
```
