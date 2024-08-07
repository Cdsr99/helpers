## Update the system's packege

```shell
sudo apt update && sudo apt upgrade -y
```

## Install Mysql Server
```shell
sudo apt-get install mysql-server-8.0
```

## Set Mysql server to be able to access from outside of the server
```shell
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```

Change the bind-address line the '127.0.0.1' to '0.0.0.0'

## Create an User
```shell
sudo mysql
CREATE USER 'new_user'@'%' IDENTIFIED BY 'password';
```
Example

```shell
CREATE USER 'admin_petrofisa'@'%' IDENTIFIED BY 'ad5asdasd56412534156s5d4';
```

## Grant Permissions

```shell
GRANT ALL PRIVILEGES ON * . * TO 'new_user'@'localhost';
GRANT ALL PRIVILEGES ON * . * TO 'admin_petrofisa'@'%';
FLUSH PRIVILEGES;
```

## Check the Firewall
```shell
sudo ufw status
```

If its able, just make sure the port 3306 its enabled.

```shell
sudo ufw status verbose 
```

Enable the port 3306.

```shell
sudo ufw allow 3306
```