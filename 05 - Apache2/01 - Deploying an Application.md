## Update the system's packege

``sudo apt update && sudo apt upgrade -y``

## Download Apache 2
``sudo apt-get install apache2``

* P.s: you can check if the page is working by searching by the computer's ip address or if its localby localhost.


## Give permission to the directory
``sudo chmod 777 /var/www/html``


## Download your project or create one

``git clone <git repository>`` 

<br>Example:<br>

``git clone git@github.com:xRodrigues/rodflix_v2.git`` 

## Run install all the dependency
`composer install`

If u don't have composer installed, run this:

`sudo apt-get install composer`