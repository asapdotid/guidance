# Reset MySQL 8 (use brew)

$ brew services stop mysql
$ pkill mysqld
$ rm -rf /usr/local/var/mysql/ # NOTE: this will delete your existing database!!!
$ brew postinstall mysql
$ brew services restart mysql
$ mysql -uroot


## setup password mysql

$ mysql_secure_installation