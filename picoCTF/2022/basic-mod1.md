## Descripcion
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/129/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Pistas
Do you know what `mod 37` means?
`mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.

## Solucion
350 63 353 198 114 369 346 184 202 322 94 235 114 110 185 188 225 212 366 374 261 213 
Aplicar modulo 37 a los numeros
17 26 20 13 3 36 13 36 17 26 20 13 3 36 0 3 3 27 33 4 2 28
Traducir con los caracteres de la descripción

## Bandera
picoCTF{R0UND_N_R0UND_ADD17EC2}

## Notas

