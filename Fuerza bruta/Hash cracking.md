# John
```
.\john-1.9.0-jumbo-1-win64\run\john.exe --wordlist=.\SecLists\Passwords\Leaked-Databases\rockyou.txt .\hash.txt
```

### Unshadow
```
.\john-1.9.0-jumbo-1-win64\run\john.exe --wordlist=.\SecLists\Passwords\Leaked-Databases\rockyou.txt .\hash.txt --format=crypt
```

# SSH Cracking sin John

```
https://github.com/readonlymaio/mm_id_rsa_bruteforce/blob/master/mm_id_rsa_bruteforce.sh
---
./mm_id_rsa_bruteforce.sh /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt id_rsa
```

# Hashcat
```
# Dentro de la carpeta de hashcat
.\hashcat.exe ..\hash.txt ..\SecLists\Passwords\Leaked-Databases\rockyou.txt -m 1800
```