(Abrir una terminal con permisos de Administrador)
Iniciar el servicio WinRM
```
Start-Service WinRM
```

Agregar DC a los Trusted Hosts
```
Set-Item wsman:\localhost\Client\TrustedHosts -Value <IP del DC>
```

Crear sesión y conectarse (opción 1)
```
New-PSSession -ComputerName <IP del DC> -Credential (Get-Credential)
```

```
Enter-PSSession <id>
```

Conectarse directamente (opción 2)
```
Enter-PSSession <IP del DC> -Credential (Get-Credential)
```

