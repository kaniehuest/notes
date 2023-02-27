https://github.com/adnanh/webhook

```
[
  {
    "id": "shell",
    "execute-command": "/tmp/shell.sh",
  }
]
```

```
sudo /path/to/webhook -hooks hooks.json -verbose
```

```
curl 192.168.1.87:9000/hooks/shell
```