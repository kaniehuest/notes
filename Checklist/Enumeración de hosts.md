Enumerar todos los puertos abiertos por TCP
```
sudo nmap -p- 10.10.10.10 -oG allPorts -T4
---
extractPorts allPorts
```

Enumerar versión y ejecutar scripts básicos
```
sudo nmap -sCV 10.10.10.10 -T4 -oN fastPorts
```

Enumerar puertos por UDP
```
sudo nmap -sU 192.168.1.96 -oG fastPortsUDP  -T4
```