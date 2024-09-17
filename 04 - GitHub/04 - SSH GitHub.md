# How to Create an SSH Key for GitHub

Follow the steps below to create and add an SSH key to GitHub:

## 1. Generate a new SSH key

Run the following command in your terminal to generate a new SSH key using the Ed25519 algorithm:

```bash
ssh-keygen -t ed25519 -C "cdsr073@gmail.com"
````
```bash
ssh-add ~/.ssh/id_ed25519
````
```bash
cat ~/.ssh/id_ed25519.pub
`````



