Configurar DNS
```
Get-DNSClientServerAddress
# Obtener InterfaceIndex
```

Establecer DC como servidor DNS
```
Set-DNSClientServerAddress -InterfaceIndex <ID anterior> -ServerAddresses <IP del DC>
```

Confirmar mirando la IP en InterfaceIndex
```
Get-DNSClientServerAddress
```

Agregar al DC
```
Add-Computer -DomainName <dominio> -Credential xyz\Administrador -Force -Restart
```
