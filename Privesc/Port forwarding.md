
# Remote port forwarding con chisel
Para ver un puerto interno de la máquina en nuestro host con chisel.

```
# Nuestra máquina
./chisel server --reverse -p 1234
---
# Máquina víctima
./chisel client 192.168.1.95:1234 R:<puerto atacante>:127.0.0.1:<puerto víctima>
```

# Local port forwarding con SSH

```
ssh jedah@10.10.10.10 -L 9999:127.0.0.1:9999
```

# Socat

```
socat tcp-listen:5000,fork tcp:127.0.0.01:7890
```

Forward puerto 1336 de la máquina a 1337 para todos
```
./socat tcp-listen:1337,reuseaddr,fork tcp:localhost:1336 &
```