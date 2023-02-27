# Credenciales
```
# intentar credenciales
anonymous:anonymous
```
# Listar archivos recursivamente
```
lftp -u <usuario>,<contraseña> -e 'find -l /var/www/html;bye' 192.168.1.136 | grep "d.w..w..w."
```