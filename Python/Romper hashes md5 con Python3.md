```python
import hashlib
for l in open("/usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt", encoding="utf-8", errors="ignore"): 
    if hashlib.md5((l.strip()+"\n").encode()).hexdigest()  == "85c73111b30f9ede8504bb4a4b682f48":
        print(l)
```