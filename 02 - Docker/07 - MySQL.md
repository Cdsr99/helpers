# Docker MySQL

## Introdução

Guia para executar um container MySQL usando Docker. O comando cria e inicia um container com a imagem oficial do MySQL.

## 1º Step - Download da imagem (opcional):

```shell
docker pull mysql:latest
```

## 2º Step - Configurar e iniciar o container:

Versão simples:

```shell
docker run --name meu-mysql -e MYSQL_ROOT_PASSWORD=<YourPassword> -p 3306:3306 -d mysql:latest
```

Versão completa (com persistência de dados):

```shell
docker run --name meu-mysql -e MYSQL_ROOT_PASSWORD=<YourPassword> -p 3306:3306 -v mysql-data:/var/lib/mysql -d mysql:latest
```

## 3º Step - Conectar ao MySQL:

```shell
docker exec -it meu-mysql mysql -u root -p
```

**Conexão externa:**
- Host: `localhost`
- Porta: `3306`
- Usuário: `root`
