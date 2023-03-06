```bash
#!/bin/bash

for host in {1..3}; do
        echo
        for port in {1..100}; do
                echo "" > /dev/tcp/172.17.0.$host/$port &&
                echo "[+] Puerto activo 172.17.0.$host:$port" & 
        done 2>/dev/null; wait
done;wait

echo

```