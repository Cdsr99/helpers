## First you need to update your system, run this comman below 
``sudo apt update & sudo apt upgrade -y``

## Then install docker
``sudo apt-get install docker docker.io``

## After install Docker u need to set your docker as a root:
``sudo groupadd docke``
``newgrp docker``
``sudo usermod -aG docker $USER``
