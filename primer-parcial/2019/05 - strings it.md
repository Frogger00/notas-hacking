## Descripcion
Can you find the flag in file without running it?

## Pistas
[strings](https://linux.die.net/man/1/strings)

## Solucion
```bash
frogger00-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
frogger00-picoctf@webshell:~$ strings strings | grep picoCTF
```

## Bandera
picoCTF{5tRIng5_1T_7f766a23}

## Notas


