#Dentro do seu projeto crie um arquivo com o nome "Dockerfile" e dentro do mesmo insira as seguintes informações

FROM node:20
WORKDIR /adonis_docker
COPY . .
RUN npm i
ENTRYPOINT node ace serve --watch 


#FROM seria o comando para buscar uma imagem já criada no Docker Hub, após os ":" seria a sua versão
#WORKDIR informa qual é o diretorio principal ou o diretorio raiz do docker
#COPY . . informa que os arquivos do diretorio atual devem ser copiados para o diretorio principal no docker (caminho setado no WORKDIR)
#RUN e ENTRYPOINT são comandos de execução

#Após criar o arquivo, basta roda o seguinte comando para criar a imagem
docker build -t caiorodrigues/adonis-docker:1 .

/*
Onde o caiorodrigues/adonis-docker seria o nome da imagem, isso poderia se chamar de qualquer outro nome.
após os : (dois pontos) seria a versão da imagem do seu docker
e o "." você estaria informando onde o mesmo deverá rodar
/**/