# phpbb-vagrant

A Vagrant machine and provisioning for phpBB development. Uses ansible for
provisioning. Unix install is easy, [Windows install is tricky](https://servercheck.in/blog/running-ansible-within-windows).
Might be easier to use a vm.

## ansible-galaxy

You need the following ansible-galaxy packages installed:

```
ansible-galaxy install geerlingguy.apache geerlingguy.mysql geerlingguy.php geerlingguy.php-mysql
```

One day, `perlmonkey.mailcatcher` will be back.

## Installation

All database credentials (username, password, database) are "phpbb".

Root MySQL password is also "phpbb".

## Adding Oracle

To add Oracle db to the vm, download the following files from the Oracle
[downloads page](http://www.oracle.com/technetwork/topics/linuxx86-64soft-092277.html):

- oracle-instantclient12.1-basic-12.1.0.2.0-1.x86_64.rpm
- oracle-instantclient12.1-devel-12.1.0.2.0-1.x86_64.rpm
- oracle-instantclient12.1-sqlplus-12.1.0.2.0-1.x86_64.rpm

Add them to a directory called "oracle" in the root of this project.
