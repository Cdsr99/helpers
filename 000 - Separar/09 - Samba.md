```shell
sudo apt update
```
```shell
sudo apt upgrade
```

sudo apt-get install samba

//Para verificar a versão do mesmo
smbd --version

//Status do Samba
sudo systemctl status smbd

//Arquivo de configuração
sudo nano /etc/samba/smb.conf

//Os comandos abaixo servem para criar uma pasta compartilhada
[*Nome da pasta*]
comment = Pasta de compartilhamento
path = *Informar o caminho*
valid users = username1, username2, ...
read only = No
browseable = yes
writeable = yes
create mask = 0700
directory mask = 0700

//Para criar usuário
sudo smbpasswd -a your_username
Digite a senha e a confirme
Obs: para cadastrar a senha o mesmo deve ser um usuário cadastrado no sistema, caso não esteja, basta usar o seguinte:
sudo useradd *user_name*

//Para finalizar, basta resetar o mesmo:
sudo systemctl restart smbd


