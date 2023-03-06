```bash
#!/bin/bash

for i in {1..255}; do
        ping -c 1 172.17.0.$i &>/dev/null && echo "Host activo $i" &
done;wait

echo

```