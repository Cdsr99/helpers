## Load balancer 

* Here is some simple example of it <br>

upstream servicos{
    server localhost:8001 weight=5;
    server localhost:8002 weight=2;
}

server{
    listen 8003;
    server_name localhost;

    location{
        proxy_pass http://servicos;
        proxy_set_header X-Real_IP $remote_addr;
    }
}


* Here are some option to use to load balance your applications:

* `least_conn` => This will send the client's request to the server who has least request or open connections 

* `round-robin` =>  This will send the client's request to the server and sequence

Both of then you need to be set on upstream, for example:

upstream servicos{
    least_conn;
    server localhost:8001 weight=5;
    server localhost:8002 weight=2;
}

## Backup Server

upstream servicos{
    server localhost:8001;
    server localhost:8002 backup;
}