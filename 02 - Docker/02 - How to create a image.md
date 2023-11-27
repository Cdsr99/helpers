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


## After seeting your image, you need to in fact create the image
``docker build -t caiorodrigues/adonis-docker:1 .``

Where:

* ``caiorodrigues/adonis-docker`` => Would be the name of the person/organization who made it and after the ``/`` is the nome of the image.
* After ``:`` it the version of the image.