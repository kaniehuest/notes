Enumerar usuarios
```
wpscan --url http://192.168.1.43 --enumerate u
```

Bruteforce a login
```
wpscan --url http://192.168.1.85/ --usernames users.txt --passwords passwd.txt
```

Enumeración
```
wpscan --url http://192.168.1.90 --api-token <token> -P /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt --detection-mode aggressive --plugins-detection aggressive -t 10
```