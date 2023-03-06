# Instala VMware tools

```
D:\setup64.exe
```

# Configurar Hostname
Entrar a sconfig
```
sconfig
```

Presionar opción 2
```
2) Nombre de equipo
```

Asignar nuevo nombre al DC
```
Escribir el nuevo nombre de equipo (En blanco=Cancelar): <nuevo nombre>
```

# Asignar IP estática
Entrar a sconfig
```
sconfig
```

Presionar opción 8
```
8) Configuración de red
```

Seleccionar índice
```
Seleccionar el índice del adaptador de red # (En blanco=Cancelar): <indice>
```

Selecionar opción 1
```
1) Establecer dirección del adaptador de red
```

Seleccionar dirección estática
```
Seleccionar (D)HCP o una dirección IP e(s)tática (En blanco=Cancelar): S
```

Indicar IP
```
Escribir una dirección IP estática (En blanco=Cancelar): <IP>
---
Ejemplo: Si la dirección anterior era 192.168.220.15 cambiar a 192.168.220.155
```

Mantener la misma máscara
```
Escribir una máscara de subred (En blanco=255.255.255.0):
```

Indicar puerta de enlace
```
Escribir la puerta de enlace predeterminada (En blanco=Cancelar): 192.168.220.2
```

# Instalar AD Server Core
```
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

# Configurar AD
```
Import-Module ADDSDeployment
```

```
Install-ADDSForest
# Ingresar nombre de dominio, ejemplo: xyz.local
# Ingresar contraseña segura:
```

# Configurar DNS
```
Get-NetIPAddress -IPAddress <IP del DC>
# Obtener ID en InterfaceIndex
```

Establecer DC como servidor DNS
```
Set-DNSClientServerAddress -InterfaceIndex <ID anterior> -ServerAddresses <IP del DC>
```

Confirmar mirando la IP en InterfaceIndex
```
Get-DNSClientServerAddress
```

