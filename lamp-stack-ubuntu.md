```sh
$ apt-get update

# Installing  Apache...
$ apt-get install apache2 apache2-utils

# Installing PHP5
$ apt-get install php5 libapache2-mod-php5

# Installing PHP5 modules
$ apt-cache search php5-
$ apt-get install php5-common php-pear php5-mcrypt php5-curl php5-gd

# Enable PHP index file for apache
$ nano /etc/apache2/mods-enabled/dir.conf
<IfModule mod_dir.c>
    DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>

$ echo "<?php phpinfo(); ?>" > /var/www/html/info.php

$ service apache2 restart

# Installing MySQL server and Installing PHP5-MySQL module
$ apt-get install mysql-server libapache2-mod-auth-mysql php5-mysql
$ mysql_install_db
$ mysql_secure_installation

$ apt-get install phpmyadmin
$ nano /etc/apache2/apache2.conf
Include /etc/phpmyadmin/apache.conf

$ service apache2 restart
$ nano /etc/phpmyadmin/apache.conf
<Directory /usr/share/phpmyadmin>
        Options FollowSymLinks
        DirectoryIndex index.php
        AllowOverride All
        [...]

$ nano /usr/share/phpmyadmin/.htaccess
AuthType Basic
AuthName "Restricted Files"
AuthUserFile /etc/apache2/.phpmyadmin.htpasswd
Require valid-user

$ service apache2 restart
```
## Ref:
* [how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-14-04]
* [how-to-install-and-secure-phpmyadmin-on-ubuntu-12-04]

[how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-14-04]: https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-14-04
[how-to-install-and-secure-phpmyadmin-on-ubuntu-12-04]: https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-phpmyadmin-on-ubuntu-12-04
