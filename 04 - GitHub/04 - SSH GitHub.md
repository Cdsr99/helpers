## To create a github's ssh keym follow the below steps: 
1) ``ssh-keygen -t ed25519 -C "cdsr073@gmail.com"``
2) Press ``Enter``
3) Create a password
4) i'm not sure about this one ``ssh-add ~/.ssh/id_ed25519``
5) If the number 4 work, just write down your password, otherwise, keeping going.
6) ``cat ~/.ssh/id_ed25519.pub``
7) Copy the ssh-key and past at Github.
