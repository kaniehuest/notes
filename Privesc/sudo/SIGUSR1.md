Correr programa que espera la señal SIGUSR1
```
Waiting SIGUSR1...
^Z
```

```
bg
```

```
ps -ef | grep <programa>
```

```
kill -SIGUSR1 <pid programa>
```

```
fg
```