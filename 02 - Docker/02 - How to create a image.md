## In the root of your project, you create a Dockerfile, below there're some exemple to how create an image


* ``FROM node:20``
* ``WORKDIR /adonis_docker``
* ``COPY . .``
* ``RUN npm i``
* ``ENTRYPOINT node ace serve --watch`` 


Where:

* ``From`` => Its the image that is going to be use, in the exemplo above its node image.
* ``WORKDIR`` => You are seeting the main root in the image that you are creating.
* ``COPY`` => You're copying all the files to your image.
* ``RUN`` => You're running some commands in the creation of the image
* ``ENTRYPOINT`` => I'm still trying to figure out.


#Após criar o arquivo, basta roda o seguinte comando para criar a imagem
docker build -t caiorodrigues/adonis-docker:1 .

/*
Onde o caiorodrigues/adonis-docker seria o nome da imagem, isso poderia se chamar de qualquer outro nome.
após os : (dois pontos) seria a versão da imagem do seu docker
e o "." você estaria informando onde o mesmo deverá rodar
/**/