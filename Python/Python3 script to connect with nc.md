Basic script:
```python
import pwn
import time

c = pwn.remote('192.168.1.81', '1337')
c.recvuntil('gift.\n')

count = 0

while count < 10001:
    count += 1
    data = c.recvuntil(b")").decode()
    c.recv()
    print(data)
    num1, num2, todo = int(data[1]), int(data[9]), data[5]

    result = 0
    if todo == "+":
        result = num1 + num2
    elif todo == "-":
        result = num1 - num2
    elif todo == "*":
        result = num1 * num2
    elif todo == "/":
        result = num1 / num2
    c.send((str(result) + "\n\r").encode())
    print(result, count)
print(c.recv().decode())
```