# Setup Selinux policy & Firewall Rule for Nginx (CentOS 7.5)


### Adding Port (flag `-a` mean add, flag `-p` mean protocol)
> semanage port -a -t http_port_t -p tcp 8888

### Check Port
> semanage port -l | grep -w http_port_t


# Config Firewall Rule

### Add Port to `public` zone and permananet `--permananet`
> firewall-cmd --zone=public --add-port=8888/tcp --permanent

### Check Port
> firewall-cmd --zone=public --list-all