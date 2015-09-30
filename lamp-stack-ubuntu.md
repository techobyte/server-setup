```sh
$ apt-get update
$ apt-get install apache2 apache2-utils
$ apt-get install php5 libapache2-mod-php5 php-pear php5-mcrypt

$ nano /etc/apache2/mods-enabled/dir.conf
<IfModule mod_dir.c>
    DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>

$ service apache2 restart
$ apt-cache search php5-
$ apt-get install php5-common php5-curl php5-gd
$ echo "<?php phpinfo(); ?>" > /var/www/html/info.php

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
