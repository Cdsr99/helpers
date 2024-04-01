sudo apt update
sudo apt upgrade

sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2022.list)"

wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc

sudo apt update

sudo apt-get install mssql-server

sudo /opt/mssql/bin/mssql-conf setup

systemctl status mssql-server --no-pager


sqlcmd -S localhost -U admin -P '@SkylineCdsr99'


#Para configurar o mesmo, para ser acessado de fora, para criar um usuário, seguindo os seguintes passos:
#Pasta Security (botão direito) -> https://prnt.sc/30SN_sDMceJB

#Crie um a senha e sete a tela, da seguinte maneira -> https://prnt.sc/769kb62PsYHj
#Aba Server Roles -> https://prnt.sc/8xzQysHBCCKM
#Aba User Mapping -> https://prnt.sc/uY5KRLZZFios
#Aba Securables -> Pode Pular
#Aba Status -> https://prnt.sc/C_doiSrFVAvS

#Basta confirmar, após isso bastará apenas permitir o acesso de fora, efetuando os seguintes passos:

#Aba o Sql Server Configuration Mananger, conforme no link -> https://prnt.sc/w_WhlLywPIBC
#Abra a opção SQL Server Network Configuration e selecione Protocols for MSSQLSERVER, conforme no link -> https://prnt.sc/PAcBsxv9sfOy

#Ative todos os protocolos e para finalizar, basta reiniciar o SQL Server ->https://prnt.sc/C_HgeOoCb7aG

#agora só ser feliz :D



# Windows

To install SQL Server on Windows Server you to install the lastest .Net Framework:

<a href="https://dotnet.microsoft.com/pt-br/download/dotnet-framework">Click here to download 4.1</a>

After that download the database:

<a href="https://www.microsoft.com/pt-br/sql-server/sql-server-downloads">Click here</a>

After its finished the installing, the system will give you an option to install MSSQL, just install it.

Now you have the database working local, its necessary that you enable to accessed from outside. To do that, just follow the nexts steps:

1) Create an user or enble one:

<a href="https://prnt.sc/4azUn2U6QEbt"> User</a>

2) The settings to the user:

<a href="https://prnt.sc/2icRICQozAvX">General</a>
<a href="https://prnt.sc/QLY-yE9RulIL">Server Roles</a>
<a href="https://prnt.sc/3kan9B5RWuMt">User Mapping</a>
<a href="https://prnt.sc/rrxCoGr2PzmN">Status</a>

Create a password and save just like above. Now you need to enable in here:

<a href="https://prnt.sc/w_WhlLywPIBC">SQL Server 2022 Configuration</a>

Enable the functions right below:

<a href="https://prnt.sc/PAcBsxv9sfOy">Protocol</a>


Remember of enable those two thing:

<a href="https://prnt.sc/F2SHJkKtCLYX">Propries</a>

<a href="https://prnt.sc/9Eu9JajCKm9h">Security</a>


<a href="https://prnt.sc/tZzk11ma6zLT">Connections</a>


To finish, restart the SQL:

<a href="https://prnt.sc/C_HgeOoCb7aG">Restart</a>