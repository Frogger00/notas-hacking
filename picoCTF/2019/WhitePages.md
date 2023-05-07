## Descripcion
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!

## Pistas
(None)

## Solucion
Abriendo el archivo como hex se observan distintos tipos de espacios
Crear un script en python para decifrar los espacios como un mensaje binario

```bash
from pwn import *

with open("whitepages.txt", "rb") as bin_file:
    data = bytearray(bin_file.read()) 
    data = data.replace(b'\xe2\x80\x83', b'0')
    data = data.replace(b'\x20', b'1')
    data = data.decode("ascii")
    print (unbits(data))
```



## Bandera
picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}

## Notas



