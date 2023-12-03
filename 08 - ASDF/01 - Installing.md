## First of all update your system 
`sudo apt updat`
`sudo apt upgrade`
`git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.12.0`
`sudo nano ~/.bashrc`

* Add as linhas abaixo no final do arquivo ~/.bashrc 

`. "$HOME/.asdf/asdf.sh"`
`. "$HOME/.asdf/completions/asdf.bash"`

* Close yout terminal and then open again

1) Download the node latest version 

`asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git`

2) Install it

`asdf install nodejs lates`
