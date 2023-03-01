## Arpscan 
```
sudo arp-scan -I <intrefaz de red> --localnet
```
ejemplo:
```
sudo arp-scan -I eth0 --localnet
```

## Fping
```
fping -aqg 192.168.1.0/24
```

## Reconocer el tipo de host por el MAC

```
macchanger -l
```

Ver estado de puerto
```
lsof -i:<número de puerto>
```

```
lsof -i:80
```

## Realizar un ping por TCP cuando la máquina no responde a ping por ICMP

```
tcping 10.10.10.10
```