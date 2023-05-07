## Descripcion
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg)

## Pistas
Wait, you can hide files inside files? But how do you find them?
Make sure to submit the flag as picoCTF{XXXXX}

## Solucion
Utilizar binwalk para extraer el contenido de la imagen
Acceder a las carpetas creadas y extraer el contenido de las imagenes extraidas
Al final se obtiene un archivo de texto con la bandera
```bash
binwalk -e dolls.jpg
binwalk -e 2_c.jpg
binwalk -e 3_c.jpg
binwalk -e 4_c.jpg 
cat flag.txt 
```

## Bandera
picoCTF{ac0072c423ee13bfc0b166af72e25b61}

## Notas



