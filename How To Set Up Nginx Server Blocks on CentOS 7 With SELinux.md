#How To Set Up Nginx Server Blocks on CentOS 7 With SELinux

Introduction
It is the largest and highest-traffic site on the Internet. In most cases, it can be used as a reverse proxy.

Uses clause nginx  server blocks The  to the manage configurations for an Individual site or domain. There is a matching system on the server. Identity VPS.

It will be up to you. It can be a draw.
Nginx server blocks on a CentOS 7 VPS. During this process, you will be requesting.

>Read Artile: `How to install nginx on CentOS 7 properly`

##Step One - Create the Directory Structure

First, we need to keep track of visitors.
Our  document root  (the top-level directory That looks Nginx AT to the find content to the serve) will of the BE set to Individual directories in the  /var/www directory. 

We will create a directory where we plan on making.
We  html will keep our actual files. This gives us some flexibility in our hosting.

The make for These CAN for We directories using the the  mkdir command (with a  -p flag That Allows us to the create a folder with a folder nested inside of IT):
>sudo mkdir -p /var/www/example/

>sudo chmod -R 755 /var/www

###nginx 403 Forbidden Error hosting in Website Apllication Directory

>chcon -Rt httpd_sys_content_t /var/www/example/

restart nginx
>systemctl restart nginx

done.