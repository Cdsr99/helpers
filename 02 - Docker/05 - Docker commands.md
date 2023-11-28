## Docker Commands

* Checking the images you have downloaded:
``docker image ls``

* Checking the dockers that are running
``docker ps``

* To exec some container, you can run: 
``docker run -d -p 80:3333 caiorodrigues/adonis-docker:1``

Where: 

1) ``-d`` => You're telling to run in a non-interactice way.
2) ``-p`` => You're informing the port that the container is going to use. Left would be outside door and the right its going to be the inside door.
3) ``caiorodrigues`` => The name of the organization ou person who create the image.
4) ``adonis-docker`` => The name of the image.
5) ``:1`` => Its the version.



* Stop all the containers that are running
``docker stop $(docker container ls -q)``

Where:

``-q`` => Informe to docker to use the ID of the machine is running.





#Para remover os dockers criados
docker container rm $(docker container ls -aq)

#Para remover as imagens do docker
docker rmi $(docker image ls -aq)  //uma opção seria add "--force"

#Para criar um espaço de memoria na máquina, basta usar o seguinte comando
docker run -it -v /home/<username>/Documents/<seu_diretorio>:<diretorio no docker> ubuntu bash

/*
Onde?
-it: serve para roda de uma forma interagida, ou seja abre o terminal do docker
-v: cria os espaços entre as maquinas (locahost e o docker)
primeiro caminho até os ":" informa o local onde você deseja salvar os arquivos na sua máquina
após os ":" seria onde você vai jogar os arquivos no docker, para os arquivos irem para sua maquina
ubuntu: seria o container, poderia ser qualquer outro, como o nosso criado por exemplo, caiorodrigues2/adonis-docker
bash: para entrar no terminal
*/


#criando volume de uma forma mais facil
docker volume create meu-volume

docker run -it -v meu-volume:<diretorio no docker> ubuntu bash

#esse "meu-volume" fica alocado no seguinte caminho no seu host /var/lib/docker

/**********************/
/*                    */
/*     Network        */
/*                    */
/**********************/

#Listando as networks
docker network ls

#Criando uma network
docker network create richpay

#criando containers na mesma rede
docker run -d --network <nome_network> ubuntu  





