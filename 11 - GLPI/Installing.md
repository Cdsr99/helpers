## First you need to update your system, run this comman below 
``sudo apt update & sudo apt upgrade -y``

1) Then install php's packages
```shell
sudo apt-get install php8.1 php8.1-mysql  php8.1-xml
```
2) Give permission
```shell
sudo chmod 777 /var/www/html/glpi/*
````
```shell
sudo apt-get install libapache2-mod-php8.1 php8.1-cli php8.1 php8.1-gd php8.1-imap php8.1-ldap php8.1-mysql php-soap php8.1-xmlrpc zip unzip bzip2 unrar-free php8.1-snmp php8.1-curl php-curl curl php-intl -y
```

3) Install MySQL
```shell
sudo apt install mysql-server-8.0 
```
4) Setting it up
```shell
sudo mysql
CREATE DATABASE glpi CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

CREATE USER 'master'@'%' IDENTIFIED BY 'uWt&&nVrbCJaHY9MV$J';

GRANT ALL PRIVILEGES ON . TO 'master'@'%';
FLUSH PRIVILEGES;

INSERT INTO glpi_users (name, password, authtype, language) VALUES ('admin.glpi', '$2y$10$ERFSQRmAVBzX9xNDtkV82.AixFN3ds6WKWQOwwUBcG2.7.U4c2hCa', 1, 'pt_BR'); #Senha admin

INSERT INTO glpi_profiles_users (users_id, profiles_id)  SELECT id, 4 from glpi_users WHERE name = 'admin.glpi';

```
