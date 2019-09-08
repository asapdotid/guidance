# How to install nginx on CentOS 7 properly

These instructions aim to provide proper and the only correct way to install nginx web server on CentOS 7.

## Prepare your system

First things first. You have to upgrade your CentOS 7 to latest release because nginx natively supports CentOS 7 >= 7.4:
> sudo yum update && yum upgrade

## Add stable nginx repository

Now that we have at least CentOS 7.4, let’s install nginx repository to our system. We import nginx package signing key and install release package which contains the nginx yum repository file.
> sudo rpm --import https://nginx.org/keys/nginx_signing.key 

next
>sudo rpm -Uvh http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm

As of this writing, EPEL repository has nginx package 1.12.2-2.el7 whereas nginx latest package is 1.12.2-1.el7_4.ngx. The actual version number is the same, but release number (-2 vs -1 in package names) is different. So if would proceed with installation, yum will install nginx from EPEL.

The nginx packages by EPEL have entirely different structure and we want stable nginx server which is packaged and maintained by nginx creators, not EPEL.

So let’s make sure that the native nginx repository has priority over the others.

Install priorities yum plugin and adjust nginx repository priority:
>sudo yum -y install yum-plugin-priorities

next

>echo 'priority=1' >> /etc/yum.repos.d/nginx.repo

Check nginx version on repo:
> yum info nginx

![Informasion Nginx version on repo](https://i.imgur.com/gpElbA1.png)

Now `yum` will prefer to install nginx from stable nginx repository. Finalise your nginx setup with:
>sudo yum -y install nginx

## Run nginx and Other Commandline
Now we are ready to run nginx:
> sudo systemctl start nginx

And don’t forget to enable it at boot time:
>sudo systemctl enable nginx

Check statud nginx:
>sudo systemctl status nginx

Check nginx version:
>nginx -v

Check nginx test configuration:
>nginx -t

Reload nginx service:
>nginx -s reload

or

> systemctl restart nginx
