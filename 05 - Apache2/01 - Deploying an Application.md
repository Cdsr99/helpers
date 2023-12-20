## Update the system's packege

``shell
sudo apt update && sudo apt upgrade -y
``

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

If you get any error, it may be php's packages/extesions, those may be these  

`sudo apt-get install php-xml php-curl -y`

After that, you can try run composer again.

## Create a configuration's file
`sudo nano /etc/apache2/sites-available/rodflix`

Configure your file like this <a href="https://github.com/Cdsr99/helpers/blob/main/05%20-%20Apache2/02%20-%20Configurations%20file.md">click here</a>

Give permission to the file following the follow steps:
`sudo a2ensite <configuration's file name>`
`sudo a2ensite rodflix.conf`
`sudo a2enmod rewrite`

## Restart apache
`sudo service apache2 restart`