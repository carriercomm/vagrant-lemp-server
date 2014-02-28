This repo contains a SH script to setup a LEMP Server { Linux + Nginx + MySQL + PHP FPM } for Phalcon PHP development environment.



### Script Contains

1. Essentials
    * git-core
    * vim
    * make, gcc, auto-conf
1. Nginx
1. MySQL
1. PHP
    * Phalcon PHP
    * php5-cli
    * php5-dev
    * php5-fpm
    * php5-mysql
    * php5-curl
    * php5-memcache
    * php5-gd
    * php5-mcrypt
    * php5-xmlrpc
    * php5-sqlite
   
***


### Setup Guide

* Make sure you have already installed Vagrant to continue. more at [vagrantup.com](http://www.vagrantup.com/downloads.html)

* **Step 1:** Cloning the repository

>you can change the path if you want to, but you will have to pay attention to the Vagrant file script path before execute it.

```
$ cd /usr/local/
$ git clone https://github.com/nancorrea/vagrant-lemp-server.git
```

* **Step 2:** Starting your VM
```
$ cd /usr/local/vagrant-lemp-server/
$ vagrant init
$ vagrant up
$ vagrant ssh
```

* **Step 3:** Executing the Script

> Make sure you are the root user otherwise some resources wont be installed.
>
>>the default password for the Vagrant root user is "vagrant"
```
$ sudo su
```

```
$ cd /var/www/
$ sh create-server.sh
```

***
### Notes for Vagrant ###

1. **Default root user pass:** "vagrant"
3. **Default correlated folder:** /usr/local/vagrant-lemp-server/www = /var/www
2. **Default VM IP:** "192.168.10.10"
4. **HTTP PORT:** *:80 (nginx)

### Notes for PHP ###

1. **Default Phalcon vhost created on VM at:** /etc/nginx/sites-available/foo-vhost
2. **PHP INFO at:** http://192.168.10.10/info.php
3. **display_errors:** on;
4. **short_open_tags:** on;
5. **added extension:** phalcon.so;

### Notes for MySQL ###

1. **default root user:** root
2. **default root pass:** root




