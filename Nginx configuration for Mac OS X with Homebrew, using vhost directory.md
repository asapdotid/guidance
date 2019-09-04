# Nginx configuration for Mac OS X with Homebrew, using vhost directory.

Check nginx services on homebrew and start:
> brew services list

Create directory for virtual host
> mkdir -p /usr/local/etc/nginx/vhost
 
Adding setup file from sites-enabled to nginx configuration `nginx.conf` on buttom file.
> include vhost/*;

Try to create virtual host in directory `vhost`

After that you can reload nginx
> brew services restart nginx
 
Please inform if you have any question to 