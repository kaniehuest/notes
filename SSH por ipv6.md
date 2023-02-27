
Ver las ipv6 de los hosts, no muestra nada
```
ip -6 neigh
```
Hacer ping o todos los hosts por ipv6 en la red
```
ping6 ff02::1
```
Arp para ver las mac de cada host según su ipv4
```
arp -e
```
Volver a listar las ipv6 y esta vez sí los muestra, se pueden diferenciar por la mac.
```
ip -6 neigh
```
Conectarse
```
ssh -6 pink@fe80::a00:27ff:fe83:3100%eth0
```
