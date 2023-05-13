## Descripcion
Smash the stackLet's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/173/vuln). You can view source [here](https://artifacts.picoctf.net/c/173/vuln.c). And connect with it using:`nc saturn.picoctf.net 51532`

## Pistas
How can you trigger the flag to print?
If you try to do the math by hand, maybe try and add a few more characters. Sometimes there are things you aren't expecting.
Run `man gets` and read the BUGS section. How many characters can the program really read?

## Solucion
Abrir el código fuente del problema
Se observa que el tamaño maximo del dato a leer es de 64
Al introducir un dato de más de 64 caracteres se obtiene la bandera

## Bandera
picoCTF{ov3rfl0ws_ar3nt_that_bad_90d2bb58}

## Notas



