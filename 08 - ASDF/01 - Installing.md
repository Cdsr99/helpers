## First of all update your system 
`sudo apt updat` <br>
`sudo apt upgrade` <br>
`git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.12.0` <br>
`sudo nano ~/.bashrc`<br>

1) Open the file "~/.bashrc" and add in the last line: 

`sudo nano ~/.bashrc`<br>

`. "$HOME/.asdf/asdf.sh"` <br>
`. "$HOME/.asdf/completions/asdf.bash"`

2) Close yout terminal and then open again

3) Download the node latest version 

`asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git`

4) Install it

`asdf install nodejs lates`
