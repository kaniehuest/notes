# Port knocking
```
cat /etc/knockd.conf
```

# Grupos importantes
```
Disk
Docker
```

# SUID
```
find / -u=s 2>/dev/null
```

# Archivos con permisos del usuario
```
find / -user <usuario> 2>/dev/null
---
find / -group <usuario> 2>/dev/null
```

# Capabilities
```
getcap -r / 2>/dev/null
```

# Library hijacking python3
```
---
import <libreria>
---
find -name <libreria>.py 2>/dev/null
```

# Path hijacking
```
Path -> /usr/local/bin:/usr/bin
---
Si un archivo corre en /usr/bin y tienes permisos de escritura en /usr/local/bin puedes hacer un path hijacking
```

# Procesos
```
ss -nlatp
---
ps -faux
```

# Tareas cron
```
/etc/cron.d
```

# Kernel
```
uname -a
```
** Linux Kernel 2.6.22 < 3.9 - 'Dirty COW ** 

# Rsync
```
cat /etc/rsyncd.auth
```

# Grub
```
ls -la /etc/grub.d/
```