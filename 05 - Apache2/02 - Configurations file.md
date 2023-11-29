## Set your virtual host

<VirtualHost *:81>
    ServerAdmin rodflix.com
    DocumentRoot /var/www/html/project_name/public
    ServerName rodflix.com

    <Directory /var/www/html/project_name/public>
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
