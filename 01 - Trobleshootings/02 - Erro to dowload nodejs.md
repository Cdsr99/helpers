## Erro to download and install the latest version of nodejs

The erro:

`asdf install nodejs latest`

Trying to update node-build... ok
Downloading node-v21.3.0-linux-x64.tar.gz...
-> https://nodejs.org/dist/v21.3.0/node-v21.3.0-linux-x64.tar.gz
error: failed to download node-v21.3.0-linux-x64.tar.gz
-> https://nodejs.org/dist/v21.3.0/node-v21.3.0-linux-x64.tar.gz
error: failed to download node-v21.3.0-linux-x64.tar.gz

BUILD FAILED (Ubuntu 23.04 using node-build 4.9.132)

Binary installation failed; try compiling from source with `--compile` flag


1) Firts of all make sure you have the `nodejs` and also `npm`

`node -v` <br>
`npm -v` <br>

If you don't have installed, just follow the script below

`sudo apt-get install nodejs`<br>
`sudo apt-get install npm`<br>

2) With everything ready to go, just follow the script below

`sudo npm install -g n`<br>
`sudo n lts`<br>

You good to good.
