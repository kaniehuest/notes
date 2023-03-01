```
mkdir -p container01/rootfs && cd container01
---
/usr/bin/runc spec
---
nano config.json
```

Copiar en la sección mounts
```
{
	"type": "bind",
	"source": "/",
	"destination": "/",
	"options": [ "rbind", "rw", "rprivate" ]
},
```

Debería verse así
```
    "mounts": [
                {
                        "type": "bind",
                        "source": "/",
                        "destination": "/",
                        "options": [ "rbind", "rw", "rprivate" ]
                },
```

Correr runc
```
sudo /usr/bin/runc run mycont
```