## Setting the server 

1) Nginx configuration's file
`` /etc/nginx/conf.d/default.conf `` 

2) In the path below, its where ngix render the application 
`` /usr/share/nginx/html/index.html ``
3) An example of setting:
```shell
server {
    listen 8080;
    server_name example.com www.example.com;

    root /var/www/html/Petrofisa;
    index index.php;

    location / {
        try_files $uri $uri/ =404;
    }

        location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php8.1-fpm.sock;
    }

    error_page 404 /404.html;
    location = /404.html {
        internal;
    }

    error_page 500 502 503 504 /50x.html;
    location = /50x.html {
        internal;
    }

    access_log /var/log/nginx/Petrofisa.access.log;
    error_log /var/log/nginx/Petrofisa.error.log;
}
```