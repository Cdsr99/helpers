# Docker Sql Server

## 1º Step download the image by running the code below:

Download the latest SQL Server image by running the following command:

```shell
docker pull mcr.microsoft.com/mssql/server
```

## 2º Set up the machine:

Set up and start the SQL Server container by running the command below. Replace <YourPassword> with a strong password of your choice:

```shell
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<Password>" -p 1433:1433 -d mcr.microsoft.com/mssql/server:2019-latest
```