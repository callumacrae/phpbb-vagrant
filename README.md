# phpbb-vagrant

A Vagrant machine and provisioning for phpBB development. Uses ansible for
provisioning.

## ansible-galaxy

You need the following ansible-galaxy packages installed:

```
ansible-galaxy install geerlingguy.apache geerlingguy.mysql geerlingguy.php geerlingguy.php-mysql
```

One day, `perlmonkey.mailcatcher` will be back.

## Installation

All database credentials (username, password, database) are "phpbb".

Root MySQL password is also "phpbb".