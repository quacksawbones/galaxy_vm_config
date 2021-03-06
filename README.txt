Things to do BEFORE it will work:

sudo firewall-cmd --add-service=http --permanent
sudo firewall-cmd --add-port=443/tcp --permanent

sudo semanage fcontext -a -t httpd_sys_content_t '/srv/galaxy/server(/.*)?'
sudo restorecon -Rv /srv/galaxy/server

