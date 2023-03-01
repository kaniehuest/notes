```
sed -e "s/-----BEGIN OPENSSH PRIVATE KEY-----/&\n/"\
    -e "s/-----END OPENSSH PRIVATE KEY-----/\n&/"\
    -e "s/\S\{64\}/&\n/g"\
    root1line > root
```
