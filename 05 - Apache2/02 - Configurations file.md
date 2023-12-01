## Set your virtual host


<VirtualHost *:81>
    ServerAdmin rodflix.com
    DocumentRoot /var/www/html/rodflix_v2/public
    ServerName rodflix.com

    <Directory /var/www/html/rodflix_v2/public>
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
