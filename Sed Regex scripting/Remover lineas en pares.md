Contenido de archivo
```
aaaaaaaaaaaaaaaaaaaa
bbbbbbbbbbbbbbbbbb
cccccccccccc
ddddddddddddddddd
```

Comando
```
cat test | sed '1~2d'
```

Resultado
```
bbbbbbbbbbbbbbbbbb
ddddddddddddddddd
```
