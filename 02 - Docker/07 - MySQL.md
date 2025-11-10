# Docker MySQL

## Introdução

Este guia mostra como executar um container MySQL usando Docker. O comando `docker run` cria e inicia um novo container com a imagem oficial do MySQL, configurando automaticamente o banco de dados e permitindo acesso externo através de uma porta mapeada.

## 1º Step - Download da imagem (opcional):

Baixe a imagem mais recente do MySQL executando o comando abaixo:

```shell
docker pull mysql:latest
```

## 2º Step - Configurar e iniciar o container:

Execute o comando abaixo para criar e iniciar o container MySQL. Substitua `<YourPassword>` por uma senha forte de sua escolha:

```shell
docker run --name meu-mysql -e MYSQL_ROOT_PASSWORD=<YourPassword> -p 3306:3306 -v mysql-data:/var/lib/mysql -d mysql:latest
```

### Explicação dos parâmetros:

- `--name meu-mysql`: Define o nome do container como "meu-mysql"
- `-e MYSQL_ROOT_PASSWORD=<YourPassword>`: Define a senha do usuário root do MySQL
- `-p 3306:3306`: Mapeia a porta 3306 do container para a porta 3306 do host (permite conexão externa)
- `-v mysql-data:/var/lib/mysql`: Cria um volume nomeado para persistir os dados do banco
- `-d`: Executa o container em modo detached (em segundo plano)
- `mysql:latest`: Usa a imagem oficial mais recente do MySQL

## 3º Step - Conectar ao MySQL:

Após iniciar o container, você pode conectar ao MySQL usando:

```shell
docker exec -it meu-mysql mysql -u root -p
```

Ou conecte-se de uma aplicação externa usando:
- **Host**: `localhost` (ou `127.0.0.1`)
- **Porta**: `3306`
- **Usuário**: `root`
- **Senha**: A senha definida no comando `docker run`

## Comandos úteis:

- **Ver logs do container**: `docker logs meu-mysql`
- **Parar o container**: `docker stop meu-mysql`
- **Iniciar o container novamente**: `docker start meu-mysql`
- **Remover o container**: `docker rm meu-mysql` (após parar)
- **Remover o volume de dados**: `docker volume rm mysql-data`
