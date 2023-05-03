## Descripcion
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled2.png)

## Pistas
[https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
Think of different ways you can "stack" images

## Solucion
Descargar las imagenes y crear un script para descifrar la flag.
```bash
from PIL import Image 
import numpy as np

imagen1 = np.array(Image.open('scrambled1.png'))
imagen2 = np.array(Image.open('scrambled2.png'))
print(imagen1)
print(imagen2)
datos = imagen1.copy() + imagen2.copy()
nueva = Image.fromarray(datos)
nueva.save('nueva.png','PNG')
```

## Bandera
picoCTF{da8fcef8}

## Notas

