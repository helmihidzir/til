# SSH key

1. In case if SSH identity suddenly not set.
```
ssh-add ~/.ssh/<private key's name>
```

2. Fixing `WARNING: UNPROTECTED PRIVATE KEY FILE`. You need to reset the permission to default: 
```
sudo chmod 600 ~/.ssh/<name of your ssh key>
```
[Source](https://medium.com/@maximbilan/ssh-keys-fixing-the-warning-unprotected-private-key-file-17fabdca7d3b)
