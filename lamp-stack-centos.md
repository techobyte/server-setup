# LAMP Stack installation on CentOS

```sh
  $  yum update
  $  rpm -Uvh https://mirror.webtatic.com/yum/el6/latest.rpm
  $  yum update
  $  yum list | mysql
  $  yum list | grep php
  $  yum list | grep mysql
  $  yum install mysql55w mysql55w-server
  $  mysql -u root
  $  yum remove mysql*
  $  yum install mysql55w mysql55w-server
  $  service mysqld start
  $  chkconfig --levels$ mysqld on
  $  mysql -u root
  $  yum install httpd
  $  service httpd start
  $  chkconfig httpd on
  $  yum install wget nano curl curl-devel
  $  yum groupinstall -y "Development Tools"
  $  yum install ntp ntpdate ntp-doc
  $  chkconfig ntpd on
  $  ntpdate pool.ntp.org
  $  service ntpd start
  $  yum install libmcrypt libmcrypt-devel libpng libjpeg
  $  yum install php55w
  $  service httpd restart
  $  nano /var/www/html/info.php
  $  yum list | grep php
  $  yum list | grep php$   $  yum install php55w-gd php55w-mbstring php55w-mysql php55w-odbc php55w-pear php55w-tidy
  $  service httpd restart
  $  curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin
  $  mkdir /mnt/web
  $  nano /mnt/web/index.php
  $  cp /etc/httpd/conf/httpd.conf /etc/httpd/conf/httpd.conf.orig
  $  nano /etc/httpd/conf/httpd.conf
  $  service httpd restart
  $  cd /mnt
  $  wget https://github.com/laravel/laravel/archive/v4.2.11.zip | unzip
  $  ll
  $  unzip v4.2.11.zip
  $  mv laravel-4.2.11/* web/
  $  ll web/
  $  cd web/
  $  php /usr/local/bin/composer.phar install
  $  cd ..
  $  chown -R apache:apache web/
  $  chmod -R$ web/
  $  nano /etc/httpd/conf/httpd.conf
  $  service httpd restart
  $  yum install php55w-mcrypt
  $  service httpd restart
  $  history
```
