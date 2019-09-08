# Nginx configuration for Mac OS X with Homebrew, using sites-enabled directory.

Check nginx services on homebrew and start:
> brew services list

Create directory for virtual host
> mkdir -p /usr/local/etc/nginx/sites-{enabled,available}

Adding setup file from sites-enabled to nginx configuration `nginx.conf` on buttom file.

> include sites-enabled/*;

Try to create virtual host in directory `sites-available` then linked to `sites-enabled`

``` bash
cd /usr/local/etc/nginx/sites-enabled
ln -s ../sites-available/example
```

After that you can reload nginx
> brew services restart nginx

Please inform if you have any question to
