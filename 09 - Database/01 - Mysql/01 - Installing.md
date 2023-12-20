## Update the system's packege

```shell
sudo apt update && sudo apt upgrade -y
``

# Install Mysql Server
```shell
sudo apt-get install mysql-server-8.0
´´

# Set Mysql server to be able to access from outside
```shell
cd  /etc/mysql/mysql.conf.d/
``
sudo nano mysqld.cnf
//"#" - Comente a linha bind-address e a linha abaixo onde o mesmo vai estar 127.0.0.1 

//Para criar um usuário no banco
sudo mysql
CREATE USER 'new_user'@'%' IDENTIFIED BY 'password';
CREATE USER 'rodflix'@'%' IDENTIFIED BY 'ad5sa86das6d54as5d4';
GRANT ALL PRIVILEGES ON * . * TO 'new_user'@'localhost';
GRANT ALL PRIVILEGES ON * . * TO 'rodflix'@'%';
FLUSH PRIVILEGES;

//Valide o Firewall
sudo ufw status

//Se estiver ativado basta validar a porta 3306
sudo ufw status verbose 

//Para liberar a porta
sudo ufw allow 3306
