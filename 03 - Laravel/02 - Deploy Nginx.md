## Atualize os pacotes
sudo apt update && sudo apt upgrade -y  

## Instale o Nginx
sudo apt-get install nginx

## Caminho de configuração

Nesse caminho você pode editar as configurações do seu serviço web. 
`` /etc/nginx/conf.d/default.conf `` <br>

No caminho abaixo segue a diretório que é renderizado pelo Nginx.<br>
`` /usr/share/nginx/html/index.html ``

## Exemplo de arquivo de configuração

``````
server {
    listen 80;

    location / {
        root /var/www/html/teste/public;
        
    }

}
``````