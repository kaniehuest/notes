
Descifrar con id_rsa
```
openssl pkeyutl -decrypt -inkey id_rsa.pem -in h4ckb1tu5.enc -out key
```

Descifrar con contraseña
```
openssl enc -aes128 -pbkdf2 -d -in file.enc -out file.txt
---
openssl enc -aes-256-cbc -d -in file.enc -out file.txt
# enter aes-128-cbc decryption password:
```